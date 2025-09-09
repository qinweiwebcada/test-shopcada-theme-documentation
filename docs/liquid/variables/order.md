# Order

{% hint style="info" %}
**Email template**\
Use `order` as the prefix when referencing variables in email templates.\
For example: `{{ order.order_id }}`
{% endhint %}


### order\_id

Return order ID



### name

Return order ID with # in front



### customer

Return [customer information](liquid/variables/account.md) in object



### billing\_address

Return customer billing address in object



### shipping\_address

Return shipping address object



### created\_at

Return order created unix timestamp, date filter can be used to format it



### checkout\_at

Return order checkout unix timestamp, date filter can be used to format it



### paid\_at

Return order paid unix timestamp, date filter can be used to format it



### modified\_at

Return order last modified unix timestamp, date filter can be used to format it



### currency

Return currency name of the order



### product\_count

Return number of product in the order



### products

Return a list of [order product](liquid/variables/order-product.md)



### product\_subtotal

Return subtotal of all the items in the order after the manual discount on the item has been applied



### line\_items

Return a list of [order line items](liquid/variables/order-line-items.md) such as sale, promotion price, rebate or additional charge



### total

Return products total + line items total excluding store credit, gift certificate, reward points and custom credit



### payable\_total

Return order total that is payable via cash / credit cards / bank transfer etc



### payments

Return a list of [order payment](liquid/variables/order-payment.md) information



### payment\_method

Return order payment method



### payment\_method\_id

Return order payment method id



### refunds

Return a list of [order refunds](liquid/variables/order-refund.md) details



### refund\_total

Return the total amount of refund



### net\_total

Return the amount that order\_total - refun&#x64;_\__&#x74;otal



### order\_status

Return order status such as pending, payment received and completed



### order\_state

Return the state of order



### order\_status\_id

Return order status id



### checkout\_comment

Return the comment that customer written during checkout



### customer\_url

Return a unique URL that the customer can use to access the order



### email

Return checkout email



### location

Return checkout channel name



### phone

Return checkout phone number



### shipping\_method

Return name of shipping method used



### shipping\_charges

Return amount of shipping charges in checkout



### shipping\_tracking

Return order shipping tracking



### is\_canceled

Return true or false if the order is canceled



### reference\_no

Return order reference number



### shipments

Return a list of [order shipments](liquid/variables/package.md) information



### return\_requests

Return a list of [order return requests](liquid/variables/return-request.md) information



### staff

Return a list of [order staff](liquid/variables/order-staff.md) information



### tax

Return a list of [order tax](liquid/variables/order-tax.md) details



### admin\_remarks

Return a list of admin comments



### is\_first\_order

Return true or false to indicate whether this is the customer's first order

