# Project

## Properties

| Property                   | Type      | Description                                            |
|----------------------------|-----------|--------------------------------------------------------|
| name                       | string    | Name of the project                                    |
| description                | string    | Description of the project                             |
| customer_id                | integer   | Customer the project concerns                          |
| instance_id                | integer   | Instance the project is installed on                   |
| time_entry_sale_models_ids | many2many | A project can be linked to one or multiple sale models |
