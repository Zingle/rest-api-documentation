# Channel Type Object
Channel Types are identifiers and communication methods.  'Phone Number' and 'Email Address' are system-wide channel types.  Services may create custom channel types.

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
type_class | string | The identifying class of the channel type.  Available options are 'PhoneNumber, 'EmailAddress', and 'UserDefined'
display_name | string | 
inbound_notification_url | string | The URL to call when an inbound message is received on a channel of this type
outbound_notification_url | string | The URL to call when an outbound message is sent on a channel of this type
allow_messages | boolean | Whether or not this channel types allows a service to communicate with contacts
is_global | boolean | Whether the channel type is scoped to a single account
