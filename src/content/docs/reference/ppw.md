---
title: Property Preservation Wizard
description: A reference page detailing how Lucidis integrates with Property Preservation Wizard.
---
## Enterprise Plan

For organizations requiring advanced features and integrations, Lucidis offers an enterprise plan that includes:
- Customizable workflows
- Enhanced data processing capabilities
- Dedicated support for integration with existing systems

## How Lucidis Ingests Work Order Documents

Lucidis integrates with Property Preservation Wizard to input work orders, work items, and bid items. The process involves:

1. **Data Extraction**: Once ingested, Lucidis employs advanced extraction techniques to identify and extract key information from the work orders. This includes:
   - Work orders
   - Work items
   - Bid items

2. **Preparation of Work Orders**: After extraction, Lucidis prepares the work orders for processing. This preparation involves organizing the extracted data into structured formats that can be easily utilized for further actions.

3. **Workflow Optimization**: By automating the ingestion and extraction processes, Lucidis significantly reduces the time required to manage work orders. What traditionally took weeks can now be accomplished in minutes, streamlining operations and enhancing productivity.

## JSON Creation from Work Order Documents

Lucidis creates structured JSON objects from the ingested work order documents. Here’s how it works:

### Work Order JSON

From the work order document, Lucidis generates a JSON object structured as follows and send directly to their API:

```json
{
"values": {
    "wo_number": "B847293838",
    "address": "16168 MAIN MARKET RD",
    "city": "BURTON",
    "state": 35,
    "zip": "44021",
    "work_type": 28813,
    "client_company": 12344,
    "date_due": "01/15/2021",
    "work_items": [{
        "id": 42931,
        "qty": 2,
        "price": 30,
        "instructions": "Some grass instructions"
        }, {
        "id": 42928,
        "qty": 3,
        "price": 10
        }]
    }
}
```
```json
{
    "report_id": 4066,
    "invoice_item_id": "42921",
    "qty": 5,
    "contractor_price": 10.92,
    "client_price": 21.96,
    "comment": "lock comment"
}
```