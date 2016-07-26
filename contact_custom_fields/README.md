# Contact Field Object

Field | Data Type | Read Only | Description
--- | --- | --- | ---
id | string | Y | Unique identifier
display_name | string | N | Field display name - shows up in the mobile app and web interfaces
data_type | string | Y | Field data type. May be string, number, boolean, date, time, or single_select_options
replacement_variable | string | Y | Placeholder used when the variable is included in a template
is_global | boolean | Y | Whether the contact field is scoped to a single service
options | array | N | Array of [Field Options]

[Field Options]: /field_options/README.md
