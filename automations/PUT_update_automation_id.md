# Update Automation 

    PUT services/:service_id/automations/:automation_id
    
Updates the the components of a single [Automation]. Returns the updated object.

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None
### Body Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | Y | The desired name of the automation
delay_minutes | int | Y | The number of minutes the automation should be delayed
conditions | array | Y | Conditions required for the automation to run
triggers | array | Y | Triggers the automation
timeout_response | object | Y | Amount of minutes until the automation times out and related message body
actions | array | Y | Actions that occur when automation runs

## Example
### Request

    PUT https://api.zingle.me/v1/services/aff8bc93-6e28-4e70-8770-defa35cdfc1b/automations/3d4f772f-d2c4-4dc1-98d0-6f23ba072758
#### Request Body
```json
{
  "display_name": "My Zing",
  "delay_minutes" : 5,
  "conditions" : [
      {
          "property" : "contact.first_name",
          "comparison_method" : "string_not_equal_to",
          "comparison_value" : "smith"
      },
      {
          "property" : "contact.vip_number",
          "comparison_method" : "string_not_equal_to",
          "comparison_value" : "null"
      }
  ],
  "triggers" : [
      {
          "type" : "keyword",
          "delay_minutes" : 0,
          "properties" : {
              "comparison_method" : "string_contains",
              "comparison_value" :  "viphelp"
          }
      },
      {
          "type" : "contact_field_event",
          "delay_minutes" : 0,
          "properties" : {
              "field" : "contact.room",
              "event_type" :  "value_changed"
          }
      },
      {
          "type" : "schedule",
          "delay_minutes" : 0,
          "properties" : {
              "frequency" : "daily",
              "time_of_day" :  "10:30:00",
              "day_of_week" :  "monday",
              "day_of_month" :  "1"
        }
      }
  ],
  "timeout_response" : {
      "minutes" : 15,
      "body" : "Sorry, try again later"
  },
  "actions" : [
      {
          "type" : "reply",
          "order" : 0,
          "is_timeout_step" : 0,
          "properties" : {
              "delay" : 0,
              "body" :  "Hey there Mr. Pizza"
          },
          "conditions" : [
              {
                  "comparison_value" : "true",
                  "comparison_source" : "{contact.is_pizza}",
                  "comparison_method" : "boolean_is"
              }
          ]
      },
      {
          "type" : "reply",
          "order" : 1,
          "is_timeout_step" : 0,
          "properties" : {
              "delay" : 0,
              "body" :  "Hey there automated guy"
          },
          "conditions" : []
      }
  ]
}
```

### Response
``` json
{
    "status": {
        "text": "OK",
        "status_code": 200,
        "description": null
    },
    "result": {
  "display_name": "My Zing",
  "delay_minutes" : 5,
  "conditions" : [
      {
          "property" : "contact.first_name",
          "comparison_method" : "string_not_equal_to",
          "comparison_value" : "smith"
      },
      {
          "property" : "contact.vip_number",
          "comparison_method" : "string_not_equal_to",
          "comparison_value" : "null"
      }
  ],
  "triggers" : [
      {
          "type" : "keyword",
          "delay_minutes" : 0,
          "properties" : {
              "comparison_method" : "string_contains",
              "comparison_value" :  "viphelp"
          }
      },
      {
          "type" : "contact_field_event",
          "delay_minutes" : 0,
          "properties" : {
              "field" : "contact.room",
              "event_type" :  "value_changed"
          }
      },
      {
          "type" : "schedule",
          "delay_minutes" : 0,
          "properties" : {
              "frequency" : "daily",
              "time_of_day" :  "10:30:00",
              "day_of_week" :  "monday",
              "day_of_month" :  "1"
        }
      }
  ],
  "timeout_response" : {
      "minutes" : 15,
      "body" : "Sorry, try again later"
  },
  "actions" : [
      {
          "type" : "reply",
          "order" : 0,
          "is_timeout_step" : 0,
          "properties" : {
              "delay" : 0,
              "body" :  "Hey there Mr. Pizza"
          },
          "conditions" : [
              {
                  "comparison_value" : "true",
                  "comparison_source" : "{contact.is_pizza}",
                  "comparison_method" : "boolean_is"
              }
          ]
      },
      {
          "type" : "reply",
          "order" : 1,
          "is_timeout_step" : 0,
          "properties" : {
              "delay" : 0,
              "body" :  "Hey there automated guy"
          },
          "conditions" : []
      }
  ]
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automation]: README.md
