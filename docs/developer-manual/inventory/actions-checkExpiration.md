# Subscription actions

## Check Expiration

Check if the subscription is expired or about to expire. 
If either of these fields is true, there will be an alert; otherwise, the alert will disappear.

### Params

| Param | Type    | Required | Description             |
|-------|---------|:--------:|-------------------------|
| id    | integer |    x     | ID of the subscription  |

### Uml

```puml
@startuml

start

if (Does the given subscription exist?) then (yes)
    if (Is the subscription expired or about to expire?) then (yes)
      :Create alert;
    else(not)
      :Disappear alert;
    endif
else (no)
  stop
endif

stop

@enduml
```
