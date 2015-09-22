# Service Object

Field | Data Type | Read Only | Description
--- | --- | --- | --- 
id | string | Y | Unique identifier
display_name | string | N | 
time_zone | string | N | Time Zone the service is located in.  This affects how times are displayed in the web and mobile app UI.
account | object | Y | [Account Object][]
plan | object | N | [Plan Object][]
channels | array | N | Array of [Service Channel Objects][]
channel_types | array | Y | Array of [Channel Type Objects][]
settings | array | N | Array of [Service Settings Objects][] representing settings on the Service
service_address | object | N | [Service Address Object][] 
created_at | UNIX timestamp | Y | Date the Account was created
updated_at | UNIX timestamp | Y | Date the Account was last updated

[Account Object]: /accounts/README.md
[Plan Object]: /plans/README.md
[Service Channel Objects]: /service_channels/README.md
[Channel Type Objects]: /channel_types/README.md
[Service Settings Objects]: /service_settings/README.md
[Service Address Object]: /service_addresses/README.md
