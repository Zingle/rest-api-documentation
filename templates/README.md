# Template Object

Field | Data Type | Read-Only | Description
--- | --- | --- | ---
id | string | Y | Unique identifier
display_name | string | N |
subject | string | N | Message subject (for communication types that support a subject field)
type | string | N | "automated_welcome", "welcome", or "general"
body | string | N | Message body
is_global | boolean | Y | Whether the Template is scoped to the Service specifically. If this is true, the Template can not be edited using the API
