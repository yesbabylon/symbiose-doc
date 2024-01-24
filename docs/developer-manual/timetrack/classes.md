# Time entry

This class extends sale\SaleEntry, this means that receivables can be generated from time entries.

## Properties

| Property             | Type    | Description                                                                       | Value(s)                                       |
|----------------------|---------|-----------------------------------------------------------------------------------|------------------------------------------------|
| description          | string  | Description of the entry                                                          |                                                |
| detailed_description | string  | Detailed description of the entry                                                 |                                                |
| project_id           | integer | Project the time entry concerns                                                   |                                                |
| customer_id          | integer | Customer the time entry concerns                                                  |                                                |
| date                 | date    | Date on which the time entry was realised                                         |                                                |
| time_start           | time    | Time when task was started                                                        |                                                |
| time_end             | time    | Time when task was finished                                                       |                                                |
| duration             | time    | Duration of the time spent on the task                                            |                                                |
| user_id              | integer | User who realised the task                                                        |                                                |
| origin               | string  | What is the origin of the time entry                                              | (backlog, email, support)                      |
| ticket_id            | integer | If origin support then a ticket id can be added to generate the ticket link       |                                                |
| ticket_link          | string  | Automatically generated ticket link from project_id.instance_id.url and ticket_id | {instance_id.url}/support/#/ticket/{ticket_id} |
| **SaleEntry**        |         |                                                                                   |                                                |
| product_id           | integer | Catalog product                                                                   |                                                |
| price_id             | integer | Product price                                                                     |                                                |
| unit_price           | float   | Unit price per hour                                                               |                                                |
| receivable_id        | integer | Generated receivable                                                              |                                                |
| has_receivable       | boolean | True if a receivable has been generated                                           |                                                |

# Project

## Properties

| Property                   | Type      | Description                                            |
|----------------------------|-----------|--------------------------------------------------------|
| name                       | string    | Name of the project                                    |
| description                | string    | Description of the project                             |
| customer_id                | integer   | Customer the project concerns                          |
| instance_id                | integer   | Instance the project is installed on                   |
| time_entry_sale_models_ids | many2many | A project can be linked to one or multiple sale models |

# Time entry sale model

## Properties

| Property     | Type      | Description                                                      |
|--------------|-----------|------------------------------------------------------------------|
| name         | string    | Name of the model                                                |
| origin       | string    | Origin the new time entry need to match for the model apply      |
| projects_ids | many2many | Projects the new time entry need to match for the model to apply |
| product_id   | integer   | Product to apply on new time entry if it matches                 |
| price_id     | integer   | Price to apply on new time entry if it matches                   |
| unit_price   | float     | Unit price to apply on new time entry if it matches              |
