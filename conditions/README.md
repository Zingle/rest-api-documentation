# Contact Object

Field | Data Type | Description
--- | --- | ---
comparison_method_code | string | Comparison method used to compare the source to the value. See below for list of supported comparison methods
comparison_source | string | Formatted string indicating a property to be evaluated. See below for details.
comparison_value | string | Specific value the comparison_source should be compared to

## Comparison Sources
{CONTACT.FIRST_NAME} | First name of the contact
{CONTACT.LAST_NAME} | Last name of the contact
{CONTACT.CREATED_AT} | Contact creaiton date
{CONTACT.PHONE_NUMBER} | Contact Phone Number
{CONTACT.EMAIL_ADDRESS} | Contact Email Address
{CONTACT.CUSTOM_FIELD.[ID]} | Value of the custom field set for a contact.  Replace [ID] with the actual ID of the contact custom field

## Comparison Methods
* boolean_is
* boolean_is_not
* boolean_is_not_set
* boolean_is_set
* date_after
* date_before
* date_is
* date_is_or_after
* date_is_or_before
* days_ago_is
* days_ago_is_less_than
* days_ago_is_more_than
* days_from_now_is
* days_from_now_is_less_than
* days_from_now_is_more_than
* day_is
* day_is_not
* number_equals
* number_greater_than
* number_greater_than_or_equal_to
* number_less_than
* number_less_than_or_equal_to
* number_not_equal_to
* string_contains
* string_does_not_contain
* string_ends_with
* string_equals
* string_not_equal_to
* string_regex_match
* string_starts_with
* hours_ago_is
* hours_ago_is_less_than
* hours_ago_is_more_than
* hours_from_now_is
* hours_from_now_is_less_than
* hours_from_now_is_more_than
* time_after
* time_at_or_after
* time_at_or_before
* time_before
* time_is
[Conditions]: /conditions/README.md
