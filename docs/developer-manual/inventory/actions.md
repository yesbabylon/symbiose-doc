# Subscription actions

## Add subscription entry

## Shift period

## Update expirations

This action updates expiration values of all subscriptions when needed, is meant to be run at every start of day.
It allows to always keep the fields *is_expired* and *has_upcoming_expiry* to a correct value.

It will:

* Sets *is_expired* to null for all subscriptions that date_to is in the past and *is_expired* is false.
* Sets *has_upcoming_expiry* to null for all subscriptions that date_to will be in the past in 30 days and *has_upcoming_expiry* is false.

The fields *is_expired* and *has_upcoming_expiry* are computed, this is why the action set their values to null and not to true.

### Params

None

### Uml

Example with one subscription for *is_expired* update:

```puml
@startuml

start

if (Is subscription "date_to" in the past?) then (yes)
  if (Is subscription "is_expired" false) then (yes)
    :Set subscription "is_expired" to NULL;
  else (no)
    stop
  endif
else (no)
  stop
endif

stop

@enduml
```

Example with one subscription for *has_upcoming_expiry* update:

```puml
@startuml

start

if (Will subscription "date_to" be the past in 30 days?) then (yes)
  if (Is subscription "has_upcoming_expiry" false) then (yes)
    :Set subscription "has_upcoming_expiry" to NULL;
  else (no)
    stop
  endif
else (no)
  stop
endif

stop

@enduml
```
