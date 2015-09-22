# Account Object

Field | Data Type | Read Only | Description
--- | --- | ---
id | string | Y | Unique identifier
display_name | string | Y | 
term_months | integer | Y | Number of months in the billing term. Applies to all child services.
current_term_start_date | UNIX timestamp | Y | Start date of the Account's current billing term
current_term_end_date | UNIX timestamp | Y | End date of the Account's current billing term
created_at | UNIX timestamp | Y | Date the Account was created
updated_at | UNIX timestamp | Y | Date the Account was last updated
