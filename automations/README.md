# Automation Object

Field | Data Type | Read-Only | Description
--- | --- | --- | ---
id | string | Y | Unique identifier
display_name | string | Y |
type | string | Y | "Escalation", "Keyword", "Self-Registration", "Survey", "Phone Call", or "Custom Automation"
status | string | Y | "active" or "inactive"
is_global | boolean | Y | Whether the Automation is scoped to the Service specifically. If this is true, the Automation can not be edited using the API
created_at | UNIX timestamp | Y | Date the Automation was created
