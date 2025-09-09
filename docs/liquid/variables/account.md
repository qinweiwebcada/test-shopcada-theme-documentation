# Customer

{% hint style="info" %}
**Email template**\
Use `account` as the prefix when referencing variables in email templates.\
For example: `{{ account.customer_id }}`
{% endhint %}

### customer\_id

Return customer ID



### user\_name

Return customer username



### last\_name

Return customer last name



### first\_name

Return customer first name



### email

Return customer email



### phone

Return customer phone number



### country\_id

Return customer country ID



### phone\_without\_dial\_code

Return customer phone number without dial code



### dob

Return customer date of birth

{{ date-output-example dob }}



### join\_at

Return customer registration date

{{ date-output-example join_at }}



### admin\_notes

Return admin notes about customer



### cards

Return list of [credit/debit card](liquid/variables/account/payment-card.md)



### orders

Return list of [orders](liquid/variables/order.md)



### cashback

Return [cashback details](liquid/variables/account/cashback-details.md)



### store\_credit

Return [store credit details](liquid/variables/account/store-credit-details.md)



### gift\_cert

Return [gift certificate details](liquid/variables/account/gift-certificate-details.md)



### default\_address

Return default [address](liquid/variables/account/address.md)



### addresses

Return list of [address](liquid/variables/account/address.md)



### points

Return [reward point details](liquid/variables/account/point-details.md)



### membership

Return list of [membership](liquid/variables/account/membership.md) information

