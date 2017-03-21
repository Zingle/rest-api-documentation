# Channel Type Object
Channel Types are identifiers and communication methods.  'Phone Number' and 'Email Address' are channel types. 

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
type_class | string | The identifying class of the channel type.  Available options are 'PhoneNumber, 'EmailAddress', and 'UserDefinedChannel'
display_name | string | 
inbound_notification_url | string | The URL to call when an inbound message is received on a channel of this type
outbound_notification_url | string | The URL to call when an outbound message is sent on a channel of this type
allow_messages | boolean | Deprecated
is_global | boolean | Deprecated
