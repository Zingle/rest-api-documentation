# Create Language Class Action

    POST services/:service_id/events/:event_id/language-class-action
    
Create an language class action on the provided language_class_detected event. The action can either be set
as the default action for the language class type, or only be executed once.  

### User Authorization Classes 
* account

## Parameters
### URI Parameters
None

### JSON Body Parameters

#### Creating a note
Field | Data Type | Required | Description
--- | --- | --- | ---
language_class_action_type_code | string | Y | The type of action that should be executed
save | bool | N | Whether or not the action should be saved as the default
workflow_id | string | N | The id of the workflow that should be executed
template_id | string | N | The id of the template that should be responded with
workflow_template_id | string | N | The id of the workflow template that should be created then executed

## Example
### Request

    POST https://api.zingle.me/v1/services/1d06e84f-8152-4de7-983d-a2d88b73734a/events/bae24ca8-8041-4d7b-b80c-d7cf097bae51/language-class-action
#### Request Body
```json
{
    "language_class_action_type_code" : "reply",
    "save" : true,
    "template_id": "95486972-873a-4ff5-834e-3830acb2ba34"
}
```

### Response
``` json
{
  "status": {
    "text": "OK",
    "status_code": 200,
    "description": "Action has been executed and saved as default"
  }
}
```

[Create Language Class Action]: /messages/POST_create_language_class_action.md
