# Service Settings Object

Field | Data Type | Read Only | Description
--- | --- | --- | ---
value | string, boolean, or UNIX timestamp | N | Settings value. Data type is dependent on the settings field data type
settings_field_option_id | integer | N | ID of the selected settings field option ID, for settings fields with options
settings_field | object | Y | [Settings Field][]

[Settings Field]: /settings_fields/README.md
