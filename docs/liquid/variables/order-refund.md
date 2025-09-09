# Order Refund

{% hint style="info" %}
**Email template**\
Use `order_refund` as the prefix when referencing variables in email templates.\
For example: `{{ order_refund.refund_id }}`
{% endhint %}

### refund\_id

Return refund ID



### order\_id

Return refund order ID



### refund\_at

Return the date of refund



### notes

Return refund notes from customer



### admin\_notes

Return refund admin notes



### refund\_method

Return method of refund



### refund\_total

Return total amount of refund



### products

Return a list of [order refund product](liquid/variables/order-refund/order-refund-product.md)



### line\_items

Return a list of [order refund line items](liquid/variables/order-refund/order-refund-line-items.md)

