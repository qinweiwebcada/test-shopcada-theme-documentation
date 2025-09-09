# Product Review Request

{% hint style="info" %}
**Email template**\
Use `review_request` as the prefix when referencing variables in email templates.\
For example: `{{ review_request.review_request_id }}`
{% endhint %}

### review\_request\_id

Return review request ID



### order\_id

Return order ID associated with the review request



### shipment\_id

Return shipment ID associated with the review request\


### notification\_id

Return notification ID linked to the review request\


### satisfaction\_level

Return satisfaction level (integer score)



### type

Return type of the review request (review or feedback)



### review\_feedback\_id

Return review request ID if type is review, feedback ID if type is feedback



### created\_by

Return user ID of who created the review request



### created\_at

Return creation timestamp of the review request

{{ date-output-example created_at }}



### review\_feedback\_url

Return review feedback url



### is\_closed

Return true or false whether the review is closed

