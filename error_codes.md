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
2900 | Service channel not found | 
3000 | Contact not found | 
3001 | Missing value for contact custom field value | 
3002 | Contact custom field not found | 
3003 | Invalid value specified for 'Is Confirmed' | 
3004 | Invalid value specified for 'Is Starred' | 
3005 | Only 'survey' and 'custom' automations may be triggered manually | 
3006 | Unable to trigger inactive automation | 
3100 | Contact channel not found | 
3101 | Contact channel missing channel type | 
3102 | Contact channel missing value | 
3103 | Contact channel missing country | 
3104 | Contact channel already assigned to another contact | 
3105 | Contact channel display name already in use for this contact | 
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
3619 | Every recipient must have a channel_value specified | 
3620 | Every recipient must have a channel_value specified | 
3621 | Every recipient must have a channel_value specified | 
3700 | Custom field value missing ID | 
3701 | Custom field not found | 
3702 | Custom field value missing option ID | 
3703 | Custom field value invalid optoin specified | 
3704 | Custom field value invalid date.  Date values must be in UNIX timestamp format | 
3705 | Custom field value missing value | 
3800 | Searching phone numbers require that a valid two-digit country code be specified as the 'country' in the URL | 
