# Time entry

A time entry records the duration of time an employee spent working on a task.
It is an extension of a sale entry, so you can generate a receivable from it that can be used to invoice a customer.

## Details

| Field       | Description                                                   | Value(s)                                 |
|-------------|---------------------------------------------------------------|------------------------------------------|
| description | Short description of the task                                 |                                          |
| user        | User who handled the task                                     |                                          |
| project     | Project the task relates to                                   |                                          |
| origin      | Origin of the task                                            | backlog/email/support                    |
| ticket      | If origin is support a ticket can be linked to the time entry |                                          |
| ticket link | Computed from project.instance.url and ticket                 | {instance.url}/support/#/ticket/{ticket} |
| date        | Date the task was handled                                     |                                          |
| start       | Start time                                                    |                                          |
| end         | End time                                                      |                                          |
| duration    | Duration of time spent                                        | {hours}:{minutes} -> 01:30               |
| product     | Catalog product                                               |                                          |
| price       | Price                                                         |                                          |
| unit price  | Per hour price                                                |                                          |
| receivable  | Generated receivable to invoice customer                      |                                          |

A time entry information can be divided in 2 parts:

1. Time entry data
    - description
    - user
    - project
    - origin
    - ticket
    - ticket link
    - date
    - start
    - end
    - duration

2. Sale data used to invoice customer
    - product
    - price
    - unit price
    - receivable

Duration, start and end times:
* The modification of the duration automatically updates the end time
* The modification of the start time and/or end time automatically updates the duration

## Actions

### Quick create

Allows to quickly create a time entry from the list view, the new time entry can then be easily modified inline.

| Where                  | How                                            |
|------------------------|------------------------------------------------|
| Time entries list view | Click on the upper right button "QUICK CREATE" |

### Create receivables

Allows to generate time entries' receivables from the list view.

| Where                  | How                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Time entries list view | 1) Select the rows with the list row checkboxes <br/> 2) Click on upper left dropdown "X SELECTED" <br/> 3) Click on "Receivable" |

### Create receivable

Allows to generate a time entry's receivable from the form view.

| Where                | How                                          |
|----------------------|----------------------------------------------|
| Time entry form view | Click on the upper right button "RECEIVABLE" |
