# Plan Object

Field | Data Type | Description
--- | --- | ---
id | string | Unique identifier
code | string | 
display_name | string | 
monthly_or_unit_price | float | Price (USD) per-month (or per room per month, when using per room pricing).
setup_price | float | Price (USD) charged one time when starting a new service using this plan
term_months | integer | Number of months per billing term
is_printer_plan | boolean | Whether this plan is used when provisioning new printer-based service
