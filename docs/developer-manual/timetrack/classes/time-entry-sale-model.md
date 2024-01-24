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
