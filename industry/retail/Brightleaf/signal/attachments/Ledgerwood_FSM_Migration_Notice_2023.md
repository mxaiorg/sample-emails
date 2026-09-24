**LEDGERWOOD REFRIGERATION SERVICES, INC.**
**Information Technology — Change Notice**

| | |
|---|---|
| Notice | IT-2023-014 |
| Subject | Field service platform migration — Servicetrack to Meridian FSM |
| Issued | January 30, 2023 |
| Cutover | March 18–19, 2023 |
| Issued by | H. Pinkney, IT Director |
| Approved by | E. Sowerby, Director of Field Operations; C. Lisle, CFO |

---

## What is migrating

| Data class | Range | Migrating |
|---|---|---|
| Work order headers (number, site, equipment, dates, status) | all history | **Yes** |
| Closed amounts and billing references | all history | **Yes** |
| Customer and site master data | all history | **Yes** |
| Equipment registry and serial numbers | all history | **Yes** |
| Technician notes and internal correspondence | **2022-01-01 forward** | **Yes** |
| Technician notes and internal correspondence | **prior to 2022-01-01** | **No** |
| Attachments on work orders | **2022-01-01 forward** | **Yes** |
| Attachments on work orders | **prior to 2022-01-01** | **No** |

## Rationale for the note cut-off

Servicetrack stored technician notes as unstructured free text with no
field-level mapping to the Meridian schema. Migrating the full note history was
quoted at eleven weeks of vendor time. The steering group elected to migrate two
years of notes and retain the remainder in the Servicetrack archive appliance for
the statutory period.

## What this means in practice

**Pre-2022 work orders will appear complete and will not be.** A pre-2022 order
will show what was done and what it cost. It will not show what the technician
observed, what was recommended, or what was said internally about it.

The Servicetrack archive appliance will be retained until **March 2025**, readable
by IT on request, subject to extension at the 2024 review.

## Not affected

The corporate mail archive is a separate system and is unaffected by this
migration. Mail retention remains indefinite.
