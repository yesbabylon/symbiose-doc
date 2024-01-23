# Timetrack

## Time entry

A time entry records the duration of time an employee spent working on a task.
It is an extension of a sale entry, so it can generate receivables that are used to invoice a customer.

## Project

A customer project categorizes the time entries, it is also used to apply specific sale models to time entries.

## Time entry sale model

A sale model allows to automatically set the sale information of a new time entry.
Its goal is to ease the creation of time entries.

Each origin (backlog/email/support) can have a default sale model to apply on new time entries from that origin.
Other sale models can be created by linking them to specific projects.
A sale model with the same origin and project than the new time entry will be applied by priority.
