# Price Match Request

{% hint style="info" %}
**Email template**\
Use `price_match_request` as the prefix when referencing variables in email templates.\
For example: `{{ price_match_request.request_id }}`
{% endhint %}

### **request\_id**

Return request ID



### request\_name

Return requester's name



### email

Return requester's email



### phone

Return requester's phone



### product\_name

Return product name



### product

Return list of [product information](liquid/variables/products.md).

&#x20;

### selected\_variant

Return list of [product variant information](liquid/variables/products/product-variant.md)



### uid

Return user ID



### requested\_price

Return requested price



### accepted\_price

Return accepted price



### external\_link

Return competitor's website link mentioned by user



### qty

Return product quantity



### model

Return SKU / Model of requested product



### valid\_until

Return validity of request in unix timestamp

{{ date-output-example valid_until }}



### status

Return status of request

1. pending
2. rejected
3. approved
4. added\_to\_cart
5. purchased
6. expired



### purchase\_link

Return purchase link of request



### request\_submitted\_at

Return request submission unix timestamp

{{ date-output-example request_submitted_at }}



### request\_accepted\_at

Return request accepted unix timestamp

{{ date-output-example request_accepted_at }}



### request\_rejected\_at

Return request rejected unix timestamp

{{ date-output-example request_rejected_at }}



### validity\_days

Return number of request validity days.

