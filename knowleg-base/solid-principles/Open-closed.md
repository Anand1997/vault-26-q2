---
tags:
  - "#ocp"
---
# Open-closed principle
The software entities should be open for extension, but closed for modification.

# Example
```python 
# FILE : payment.py
def processor(method,amount):
	match method:
		case "credit_card":
			charge_card(amount)
		case "cash"
			charge_cash(amount)
```
> [!important] New requirement => Added UPI payment
```python
# FILE : payment.py
def processor(method,amount):
	match method:
		case "credit_card":
			charge_card(amount)
		case "UPI":
			charge_upi(amount)
		case "cash"
			charge_cash(amount)
```
> [!warning] Not closed for modification while extending, need to change existing file.
```python 
# FILE : payment.py
class PaymentMethod():
	def process(amount):
		pass

# FILE : payment_credit_card.py
class CreditCardPayment(PaymentMethod):
	def process(amount):
		print(f"> {amount} Processed using Credit Card ...")
		return 

# FILE : payment_UPI_card.py
class UPIPayment(PaymentMethod):
	def process(amount):
		print(f"> {amount} Processed using UPI ...")
		return 

# FILE : payment_cash.py
class CashPayment(PaymentMethod):
	def process(amount):
		print(f"> {amount} Processed using Cash ...")
		return 
```
> [!done] No need to change old code to add new code for new requirement.

