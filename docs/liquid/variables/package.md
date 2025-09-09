# Order Shipment

{% hint style="info" %}
**Email template**\
Use `package` as the prefix when referencing variables in email templates.\
For example: `{{ package.shipment_id }}`
{% endhint %}

### shipment\_id

Return shipment id



### order\_id

Return order id in shipment



### shipping\_method\_name

Return shipping method name



### shipping\_status

Return shipping status&#x20;



### tracking\_number

Return shipment tracking number



### collection\_outlet

Return [outlet](liquid/variables/outlet.md) information on collection



### created\_at

Return timestamp of shipment created



### shipped\_at

Return shipped timestamp



### modified\_at

Return timestamp of last modification



### products

Return a list of [order shipment product](liquid/variables/package/order-shipment-product.md)



### total\_qty

Return total product quantity of shipment

