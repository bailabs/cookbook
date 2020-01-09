# ERPNext Cookbook

## get_cash_bank_account(...)
Get the account associated under `Mode of Payment` doctype
```python
from erpnext.accounts.doctype.sales_invoice.sales_invoice import get_bank_cash_account
...
account = get_bank_cash_account('Cash', company)
...
```
