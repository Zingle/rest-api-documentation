# Service Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
display_name | string | 
time_zone | string | Time Zone the service is located in.  This affects how times are displayed in the web and mobile app UI.
account | object | [Account Object][]
plan | object | [Plan Object][]
channels | array | Array of [Service Channel Objects][]
channel_types | array | Array of [Service Channel Objects][]
settings | array | Array of [Custom Field Values Objects][] representing settings on the Service
created_at | UNIX timestamp | Date the Account was created
updated_at | UNIX timestamp | Date the Account was last updated

[Account Object][]: /accounts/README.md
[Plan Object][]: /plans/README.md
[Service Channel Objects][]: /service_channels/README.md
[Channel Type Objects][]: /channel_types/README.md
