# Reservations

{% hint style="info" %}
**Email template**\
Use `uc_pos_reserve` as the prefix when referencing variables in email templates.\
For example: `{{ uc_pos_reserve.reservation_id }}`
{% endhint %}

### reservation\_id

Return reservation ID



### customer\_id

Return customer ID



### product\_id

Return product ID



### selected\_sku

Return selected product SKU



### product\_name

Return product name



### product\_image

Return product image URL



### product\_price

Return product price



### product\_options

Return product options/attributes



### product

Return [product](liquid/variables/products) information



### outlet

Return [outlet](liquid/variables/outlet.md) information



### status

Return reservation status



### created\_at

Return reservation creation date

{{ date-output-example created_at }}



### approved\_at

Return reservation approval date

{{ date-output-example approved_at }}



### collected\_at

Return reservation collected date

{{ date-output-example collected_at }}



### expire\_at

Return reservation expiry date

{{ date-output-example expire_at }}



### reminded\_at

Return reservation reminder date

{{ date-output-example reminded_at }}



### remarks

Return remarks or notes on the reservation



### allow\_cancel

Return true or false whether the reservation can be cancelled



