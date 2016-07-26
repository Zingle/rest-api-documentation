# Service Object

Field | Data Type | Read Only | Description
--- | --- | --- | --- 
id | string | Y | Unique identifier
display_name | string | N | 
business_name |  string | N | Name used in templates to replace the BUSINESS_NAME placeholder
time_zone | string | N | Time Zone the service is located in.  This affects how times are displayed in the web and mobile app UI.
account | object | Y | [Account] object
plan | object | N | [Plan] object
channels | array | N | Array of [Service Channel] objects
channel_types | array | Y | Array of [Channel Type] objects
contact_labels | array | Y | Array of [Contact Labels]
contact_custom_fields | array | Y | Array of [Contact Custom Fields]
templates | array | Y | Array of [Templates]
automations | array | Y | Array of [Automations]
settings | array | N | Array of [Service Settings] objects representing settings on the Service
service_address | object | N | [Service Address] object
created_at | UNIX timestamp | Y | Date the Account was created
updated_at | UNIX timestamp | Y | Date the Account was last updated

[Account]: /accounts/README.md
[Plan]: /plans/README.md
[Service Channel]: /service_channels/README.md
[Channel Type]: /channel_types/README.md
[Service Settings]: /service_settings/README.md
[Service Address]: /service_addresses/README.md
[Contact Label]: /labels/README.md
[Contact Custom Fields]: /contact_custom_fields/README.md
[Templates]: /templates/README.md
[Automations]: /automations/README.md
