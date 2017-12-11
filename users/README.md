# User Object

Field | Data Type | Read Only | Description
--- | --- | --- | --- 
id | string | Y | Unique identifier
username | string | Y | The user's username
title |  string | Y | Mr., Mrs., etc.
email | string | Y | The user's email address
status | string | Y | The user's current status
first_name | string | Y | The user's first name
last_name | string | Y | The user's last name
phone_number | string | Y | The user's phone number
avatar_uri | string | N | The asset uri of the user's avatar
account_uuids | array | Y | Array of [Account Ids]
service_uuids | array | Y | Array of [Service Ids]