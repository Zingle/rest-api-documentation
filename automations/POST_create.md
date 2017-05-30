# Create Automation

    POST services/:service_id/automations
    
Creates a new [Automation] for the specified Service and returns the newly-created object

### User Authorization Classes 
* account

## Parameters
### URI Parameters
Field | Data Type | Required | Description
--- | --- | --- | ---
display_name | string | Y | The desired name of the automation
timeout_minutes | int | Y | The number of minutes the automation should be delayed
conditions | array | Y | Conditions required for the automation to run
triggers | array | Y | Triggers the automation
timeout_response | object | Y | Amount of minutes until the automation times out and related message body
actions | array | Y | Actions that occur when automation runs



## Example
### Request

    POST https://api.zingle.me/v1/services/aff7bc93-6e28-4e70-8770-defa35cdfc1b/automations

#### Request Body
```json
{
  "display_name": "My Zing",
  "status": "inactive",
  "triggers": [
    {
      "type": "first_message",
      "properties": {
        "contact_disposition": "unknown",
        "delay": 0
      }
    },
    {
      "type": "keyword",
      "properties": {
        "comparison_method_code": "string_contains",
        "comparison_value": "viphelp",
        "delay": 0
      }
    },
    {
      "type": "label_event",
      "properties": {
        "field": "3801e007-3479-464e-9d89-e124bffa35ea",
        "event_type": null,
        "delay": 0
      }
    },
    {
      "type": "contact_field_event",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e",
        "event_type": "value_set",
        "delay": 0
      }
    },
    {
      "type": "contact_name_event",
      "properties": {
        "field": "first_name",
        "event_type": "value_set",
        "delay": 0
      }
    },
    {
      "type": "escalation",
      "properties": {
        "unconfirmed_minutes": 15
      }
    }
  ],
  "actions": [
    {
      "type": "reply",
      "order": "1",
      "properties": {
        "body": "Thank you for reaching out, we will do what we can to assist you",
        "delay_minutes": "0"
      },
      "conditions": [
        {
          "property": "contact.phone_number",
          "comparison_method_code": "string_contains",
          "compare_data_to": "555",
          "sort_order": "1"
        }
      ]
    },
    {
      "type": "feed_mark_read",
      "order": "2",
      "properties": [],
      "conditions": [
        {
          "property": "contact.created_date",
          "comparison_method_code": "days_ago_is",
          "compare_data_to": "1",
          "sort_order": "1"
        }
      ]
    },
    {
      "type": "reply_and_wait",
      "order": "3",
      "properties": {
        "body": "Is there anything else we can assist you with?"
      },
      "conditions": []
    },
    {
      "type": "send_sms",
      "order": "4",
      "properties": {
        "body": "{first_name}, thank you for your text. We will be with you in {response_time}",
        "to": "8052805605",
        "delay_minutes": "0"
      },
      "conditions": []
    },
    {
      "type": "send_email",
      "order": "5",
      "properties": {
        "body": "We hope you enjoyed your experience.",
        "to": "test@test.com",
        "subject": "Thank You"
      },
      "conditions": []
    },
    {
      "type": "contact_delete",
      "order": "6",
      "properties": [],
      "conditions": []
    },
    {
      "type": "contact_field_value_set",
      "order": "7",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "type": "contact_field_value_remove",
      "order": "8",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "type": "feed_mark_unconfirm",
      "order": "9",
      "properties": [],
      "conditions": []
    },
    {
      "type": "forward_to_service",
      "order": "10",
      "properties": {
        "body": "This guest requires your services",
        "service_id": "2"
      },
      "conditions": []
    },
    {
      "type": "print",
      "order": "11",
      "properties": {
        "body": "What"
      },
      "conditions": []
    },
    {
      "type": "reply_wait_save_contact_field_value",
      "order": "12",
      "properties": {
        "body": "What is your room number??",
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "type": "save_data",
      "order": "13",
      "properties": {
        "data": "{first_name}, thank you for your text. We will be with you in {response_time}",
        "variable_name": "Variable 1"
      },
      "conditions": []
    },
    {
      "type": "send_web_service_call",
      "order": "14",
      "properties": {
        "request_data": "",
        "web_service_end_point": "http://endpoint.com",
        "response_value": "{}"
      },
      "conditions": []
    },
    {
      "type": "set_email_address",
      "order": "15",
      "properties": {
        "value": "test@zingle.com"
      },
      "conditions": []
    }
  ],
  "timeout_actions": [
    {
      "type": "feed_mark_read",
      "order": "2",
      "properties": [],
      "conditions": [
        {
          "property": "contact.created_date",
          "comparison_method_code": "days_ago_is",
          "compare_data_to": "1",
          "sort_order": "1"
        }
      ]
    }
  ],
  "timeout_minutes": 15
}
```

### Response
``` json
{
  "uuid": "dd6e3805-f503-41f6-805b-b87d4dcd397a",
  "display_name": "My Zing",
  "status": "inactive",
  "triggers": [
    {
      "id": "8284239e-b0ba-4254-b1c6-f7d319ab6fba",
      "type": "first_message",
      "properties": {
        "contact_disposition": "unknown",
        "delay": 0
      }
    },
    {
      "id": "2c1b8385-f780-429a-a9c3-34e278fe5c9d",
      "type": "keyword",
      "properties": {
        "comparison_method_code": "string_contains",
        "comparison_value": "viphelp",
        "delay": 0
      }
    },
    {
      "id": "86f8708f-df07-429b-bf4e-0875c9a67f5f",
      "type": "label_event",
      "properties": {
        "field": "3801e007-3479-464e-9d89-e124bffa35ea",
        "event_type": null,
        "delay": 0
      }
    },
    {
      "id": "587f8ff7-2e6a-425c-a1c7-20ad77524a8f",
      "type": "contact_field_event",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e",
        "event_type": "value_set",
        "delay": 0
      }
    },
    {
      "id": "ee55b2a9-781e-4c14-80bd-e26114583512",
      "type": "contact_name_event",
      "properties": {
        "field": "first_name",
        "event_type": "value_set",
        "delay": 0
      }
    },
    {
      "id": "40c31ae5-0801-4858-ad4c-14b0d2c071ce",
      "type": "escalation",
      "properties": {
        "unconfirmed_minutes": 15
      }
    }
  ],
  "actions": [
    {
      "id": "cd57e4ef-e6e1-48d3-9699-c316b224ac72",
      "type": "reply",
      "order": "1",
      "properties": {
        "body": "Thank you for reaching out, we will do what we can to assist you",
        "delay_minutes": "0"
      },
      "conditions": [
        {
          "id": 47,
          "property": "contact.phone_number",
          "comparison_method_code": "string_contains",
          "compare_data_to": "555",
          "sort_order": "1"
        }
      ]
    },
    {
      "id": "8749860c-7aa2-4b6c-9547-5cb7055c6db3",
      "type": "feed_mark_read",
      "order": "2",
      "properties": [],
      "conditions": [
        {
          "id": 48,
          "property": "contact.created_date",
          "comparison_method_code": "days_ago_is",
          "compare_data_to": "1",
          "sort_order": "1"
        }
      ]
    },
    {
      "id": "1e27fb12-832f-4e6a-9f0c-8b346a48bfa3",
      "type": "reply_and_wait",
      "order": "3",
      "properties": {
        "body": "Is there anything else we can assist you with?"
      },
      "conditions": []
    },
    {
      "id": "b24b72b4-cc35-4c7c-9eb9-a2642107149b",
      "type": "send_sms",
      "order": "4",
      "properties": {
        "body": "{first_name}, thank you for your text. We will be with you in {response_time}",
        "to": "8052805605",
        "delay_minutes": "0"
      },
      "conditions": []
    },
    {
      "id": "ae7dc314-23d5-4a6e-bf25-0cfdf2deb7c6",
      "type": "send_email",
      "order": "5",
      "properties": {
        "body": "We hope you enjoyed your experience.",
        "to": "test@test.com",
        "subject": "Thank You"
      },
      "conditions": []
    },
    {
      "id": "a6a3ce7f-7af3-4c58-a4e2-0abddc31077c",
      "type": "contact_delete",
      "order": "6",
      "properties": [],
      "conditions": []
    },
    {
      "id": "a7a1aece-2a34-4449-b1b1-6f082821e21b",
      "type": "contact_field_value_set",
      "order": "7",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "id": "b3bf4fff-a74b-4ec9-a44d-7362802e9e58",
      "type": "contact_field_value_remove",
      "order": "8",
      "properties": {
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "id": "a2f767d7-a505-479d-8949-0e8306a15b43",
      "type": "feed_mark_unconfirm",
      "order": "9",
      "properties": [],
      "conditions": []
    },
    {
      "id": "6e52d23f-4350-4e7c-9858-1a166433a6ed",
      "type": "forward_to_service",
      "order": "10",
      "properties": {
        "body": "This guest requires your services",
        "service_id": "2"
      },
      "conditions": []
    },
    {
      "id": "8636b622-c3e9-44b9-9028-1b50885e49b0",
      "type": "print",
      "order": "11",
      "properties": {
        "body": "What"
      },
      "conditions": []
    },
    {
      "id": "e702e622-2154-4b07-9b8f-6d12460cbe1a",
      "type": "reply_wait_save_contact_field_value",
      "order": "12",
      "properties": {
        "body": "What is your room number??",
        "field": "857305be-c77b-4c96-bfd3-47f0b8731e3e"
      },
      "conditions": []
    },
    {
      "id": "ea842411-5e9d-44be-9b7e-39be4ba9cc1c",
      "type": "save_data",
      "order": "13",
      "properties": {
        "data": "{first_name}, thank you for your text. We will be with you in {response_time}",
        "variable_name": "Variable 1"
      },
      "conditions": []
    },
    {
      "id": "85160798-54aa-411a-9fcc-f19e285a05a5",
      "type": "send_web_service_call",
      "order": "14",
      "properties": {
        "request_data": "",
        "web_service_end_point": "http://endpoint.com",
        "response_value": "{}"
      },
      "conditions": []
    },
    {
      "id": "00ed1c19-ae1d-4676-be1a-ba126272c1ce",
      "type": "set_email_address",
      "order": "15",
      "properties": {
        "value": "test@zingle.com"
      },
      "conditions": []
    }
  ],
  "timeout_actions": [
    {
      "id": "8749860c-7bb2-4b6c-9547-5cb7055c6mf6",
      "type": "feed_mark_read",
      "order": "2",
      "properties": [],
      "conditions": [
        {
          "id": 48,
          "property": "contact.created_date",
          "comparison_method_code": "days_ago_is",
          "compare_data_to": "1",
          "sort_order": "1"
        }
      ]
    }
  ],
  "timeout_minutes": 15
}
```

[Overview - Request Modifiers]: /README.md#request-modifiers
[Automation]: README.md
