# Evaluating mxMCP Email Search: The Marchwood Benchmark

**Run · August 19, 2026 · Result: 24 / 24 — passed**

## Abstract

mxHERO's `email_search` connector was evaluated against an adversarial retrieval
benchmark of 6,000 messages, in which a single decisive document is surrounded by
approximately 155 purpose-built decoys engineered to defeat naive search — a
duplicate file number at a second office, five firms sharing a name, and a
near-identical letter that expired and would invert the correct answer. Four
questions were run blind and scored on recall, precision and correctness of the
final verdict. The connector scored 24 of 24, surfacing the critical document at
rank 4 on the first search and citing zero decoys across all four answers. On the
query designed to force a collision between two matters sharing an identifier, it
disclosed the ambiguity unprompted rather than merging them. The evaluation
supports the commercial claim that an email archive can answer questions an
organization's system of record gets wrong. One operational dependency was
identified: retrieval quality degrades sharply when the connector's identifier-
pinning parameter is omitted, which argues for enforcing it in agent
configuration rather than leaving it to model discretion.

## What was tested

mxHERO's `email_search` connector was scored against a purpose-built adversarial
benchmark: a 6,000-message synthetic email archive modeled on an SEC enforcement
matter. Buried in it is a single decisive document — a June 2, 2011 letter in
which a registrant's compliance officer accepts a finding and gives a written
undertaking "without an expiration date." Fourteen years later, that letter is
the difference between a $4.3 million enforcement action collapsing and a $2.15
million settlement.

The archive is built to punish retrieval that merely looks good. Around the
40-message story thread sit roughly 155 hand-built decoys: a second examination
carrying the identical file number at a different regional office, five firms
sharing the registrant's name, a near-identical undertaking letter dated two days
earlier at a different adviser — one that *expired*, and would invert the answer
if cited — and the same author writing the same kind of letter for a different
employer. The remaining ~5,800 messages are realistic bulk traffic.

Four queries were run blind against the live connector, then scored on three
independent axes — recall (did it find the right documents), precision (did it
avoid the decoys), and verdict (was the final answer correct). Two points per
axis, four queries, 24 points available.

## Results

The connector scored **full marks on every axis of every query**. The critical
document surfaced at rank 4 on the very first search, with its signed PDF
attachment intact. Zero decoys were cited across all four answers.

| Query | Recall | Precision | Verdict |
|---|---|---|---|
| Was there a written commitment? | ✅ | ✅ | ✅ |
| Why does the system of record disagree? | ✅ | ✅ | ✅ |
| Retrieve everything on file 2011-0447 | ✅ | ✅ | ✅ |
| Why did the failure recur, and who is responsible? | ✅ | ✅ | ✅ |

The hardest query was the third. Two entirely separate matters share the file
number by design. Rather than silently merging them — the failure mode the test
was built to catch — the connector disclosed the ambiguity unprompted, naming the
two counterparties and warning that the identifier is unique only within the
office that issued it. Correct disambiguation followed on a scoped second pass.

## Why this matters commercially

The demo claim is that an email archive answers questions an organization's
system of record gets wrong. This benchmark makes that claim falsifiable. Here,
both parties' case systems had lost the correspondence in a 2016 platform
migration, and every person who negotiated it had left. The archive was the only
surviving witness — and the connector found it, alongside a second document
showing the counterparty had already honored the commitment once, unprompted, in
2013. That second document is what converts "a document was found" into "they
already agreed, twice."

## One engineering finding

Search quality depends materially on the connector's `Pin` parameter, which
guarantees documents containing a specific identifier appear in results. One
query was deliberately run without it: 48 of 50 returned messages were noise, and
the two relevant hits survived only because the date filter was narrow. The same
question with `Pin` set returns the answer at rank 1. This is worth encoding as
default agent behavior rather than leaving to model discretion.

## Sources

All email and attachment contect used in this test, including grading key and build notes can be found in the following GitHub repository:

[GitHub - gov/SEC](https://github.com/mxaiorg/sample-emails/tree/main/industry/gov/SEC)
