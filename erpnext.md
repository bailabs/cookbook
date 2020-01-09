# ERPNext Cookbook
The following are the common patterns to using/modifying ERPNext

## get_cash_bank_account(...)
Get the account associated under `Mode of Payment` doctype
```python
from erpnext.accounts.doctype.sales_invoice.sales_invoice import get_bank_cash_account
...
account = get_bank_cash_account('Cash', company)
...
```

## override core properties
Override the core DocField properties
```python
frappe.db.sql("""
    UPDATE `tabDocField` 
    SET set_only_once = 0
    WHERE parent = 'Patient'
    AND fieldname = 'customer'
""")
frappe.db.commit()
```

