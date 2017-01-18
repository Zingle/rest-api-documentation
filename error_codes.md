# Error Codes
The following is a list of all error codes that the Zingle REST API may return. 

Error Code | Description | Explanation
--- | --- | ---
2600 | Server error | An unspecified error has occurred. This is likely our fault.
2601 | Authentication failed | Your username and password are incorrect.
2602 | Permission denied | Authentication was succesful but you do not have permission to the account or service you're trying to access.
2603 | Invalid page requested.  Valid pages must be greater than 0. | You've specified a `page` GET variable less than zero
2604 | Invalid body content. Check that your request is valid JSON | The body of your PUT or POST request isn't valid JSON.  It's likely the JSON is malformed.  See the 9(JSON Spec)[http://www.json.org/].
2605 | Unknown channel type | The channel_type_id you specified isn't valid 
2606 | Invalid phone number format | The phone number given isn't valid (valid formats may change depending on the country)
2607 | Invalid email address format | The email address format isn't valid
2608 | Unknown two-character country code | 
2609 | Invalid sort direction specified. Valid sort directions are 'asc' and 'desc'. | 
2610 | Invalid phone number search pattern.  Valid search patterns contain only numbers and asterisks | 
2611 | Invalid page_size requested.  Valid page_sizes must be greater than 0 and less than 1000 | 
2612 | Invalid value specified for is_global.  Value must be 'true' or 'false' |
2613 | You must include the HTTP header x-zingle-contact-id for this request
2614 | You need account-class access to use this resource
2615 | The contact specified in the x-zingle-contact-id header does not have access to the requested resource 
2700 | Account not found | The account you're trying to access doesn't exist
2800 | Service not found | The service you're trying to access doesn't exist
2801 | Invalid service plan | The service plan you've speficified isn't valid
2802 | Invalid time zone | The time zone you've speficified isn't valid
2803 | You do not have permission to cancel services | 
2804 | Missing service plan | 
2805 | Missing service time zone | 
2806 | Missing service display name | 
2807 | Missing service address | 
2808 | Invalid two-digit state code | 
2809 | Invalid two-digit country code | 
2810 | Missing postal code | 
2811 | Missing city | 
2812 | Invalid account specified for service | 
2813 | Missing country in service_address | 
2900 | Service channel not found | 
2901 | channel_type_id required | 
2902 | Channels of this type can not be assigned to services | 
2903 | value is required | 
2904 | A service channel with that display_name already exists | 
2905 | Error while provisioning the phone number | 
2906 | Unknown channel type | 
2907 | The chosen country does not support phone number provisioning | 
2908 | Country is required when provisioning phone numbers | 
2909 | The specified email domain is not permitted | 
2910 | The specified email is already in use | 
2911 | The specified phone number is already in use | 
2912 | That channel is already assigned to a service | 
2913 | Service channel format is not valid for the specified type | 
3000 | Contact not found | 
3001 | Missing value for contact custom field value | 
3002 | Contact custom field not found | 
3003 | Invalid value specified for 'Is Confirmed' | 
3004 | Invalid value specified for 'Is Starred' | 
3005 | Only 'survey' and 'custom' automations may be triggered manually | 
3006 | Unable to trigger inactive automation | 
3007 | Contact is already in an automation | 
3008 | Label not attached to contact. Nothing to detach. |
3009 | Invalid value specified for 'Is Closed'. Value must be 'true' or 'false'
3010 | Channels must be an array of channel objects
3011 | First name, last name, title, email addresses, and phone numbers are not editable on locked contacts
3012 | You can not use the return_existing option when specifying zero or multiple channels
3013 | Workflows cannot be triggered for email channels 
3100 | Contact channel not found | 
3101 | Contact channel missing channel type | 
3102 | Contact channel missing value | 
3103 | Contact channel missing country | 
3104 | Contact channel already assigned to another contact | 
3105 | Contact channel display name already in use for this contact | 
3106 | Contact channel display name must be 'HOME','BUSINESS', or 'MOBILE' | 
3107 | Service channel format is not valid for the specified type | 
3200 | Custom field not found | 
3201 | Unable to modify global custom field | 
3202 | Custom field display name already in use | 
3203 | Custom field missing display name | 
3204 | Custom field option missing value | 
3205 | Custom field option missing display name | 
3300 | Template not found | 
3301 | Unable to modify global template | 
3302 | Invalid template type specified | 
3303 | Template display name is already in use | 
3304 | Template missing display name | 
3305 | Template missing body | 
3306 | Template missing type | 
3400 | Label not found | 
3401 | Unable to modify global label | 
3402 | Label display name is already in use | 
3403 | Label missing display name | 
3404 | Label missing background color | 
3405 | Label missing text color | 
3406 | Invalid color specified.  Valid colors must be in hexadecimal format | 
3500 | Automation not found | 
3501 | Invalid automation status specified | 
3600 | Message not found | 
3601 | Message 'read at' date invalid. Valid dates must be in UNIX timestamp format | 
3602 | Sending a message requires a body or attachments to be specified | 
3603 | channel_type_ids is required and should be an array of strings | 
3604 | Multiple channel_type_ids can only be specified when the recipient_type is 'label' | 
3605 | sender_type is required and must be one of 'service' or 'contact' | 
3606 | ecipient_type is required and must be one of 'service', 'contact', or 'label' | 
3607 | recipients is required and must be an array with at least one objectd | 
3608 | sender is required and must be an object | 
3609 | Every recipient must have a channel_value specified | 
3610 | Either the sender or recipient must be a service | 
3611 | channel_type_id {channel_type_uuid} is not valid | 
3612 | Invalid label '{correspondent_id}' | 
3613 | '{correspondent_channel_value}' is not a valid {channel_type_display_name} | 
3614 | Invalid contact '{correspondent_id}' specified for {channel_type_display_name} | 
3615 | Channel is already assigned to another contact | 
3616 | Invalid service specified for {correspondent_type} | 
3617 | No channel {correspondent_channel_value} found for the specified channel types | 
3618 | Multiple channels found for '{channel_value}'.  Narrow your list of channel_type_ids and retry | 
3619 | Attachments must be an arry of attachment objects | 
3620 | Attachment missing content_type | 
3621 | Attachment base64 isn't valid | 
3622 | Sender channel_value is required | 
3623 | Attachments are not permitted when sending to labels | 
3624 | Invalid content_type | 
3625 | Messages can't be sent from the specified sender type to the specified recipient type using the specified channel type | 
3626 | Sending to Labels only supports SMS messages at this time | 
3700 | Custom field value missing ID | 
3701 | Custom field not found | 
3702 | Custom field value missing option ID | 
3703 | Custom field value invalid optoin specified | 
3704 | Custom field value invalid date.  Date values must be in UNIX timestamp format | 
3705 | Custom field value missing value | 
3706 | Boolean custom fields must have value 'true' or 'false'e | 
3800 | Searching phone numbers require that a valid two-digit country code be specified as the 'country' in the URL | 
3900 | Plan not found | 
4000 | Channel type not found | 
4001 | Channel type display_name is required | 
4002 | allow_messages must have value 'true' or 'false' | 
4003 | priority must be an integer | 
4004 | The supplied notification URL is not valid | 
4005 | You can not modify a global channel type | 
4006 | Channel type creation has been removed from the API.  Use the 'chat' channel type for all IP communication
4007 | Channel type deletion has been removed from the API.  Use the 'chat' channel type for all IP communication
5000 | Channel filter must include both channel_type_id and channel_value
6000 | service_ids is required and must be an array of service IDs
6001 | operating_system must be ios, android, or windows
6002 | device_identifier is required
7000 | Only message and note event type creation is allowed
7001 | contact_id is required
7002 | Contact not found
7003 | Event not found
7004 | The note body can not be blank
