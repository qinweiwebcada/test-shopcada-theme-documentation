# Product Review

{% hint style="info" %}
**Email template**\
Use `product_review` as the prefix when referencing variables in email templates.\
For example: `{{ product_review.review_id }}`
{% endhint %}

### review\_id

Return review ID



### nid

Return product ID



### order\_id

Return order ID associated with the review



### order\_product\_id

Return order product ID associated with the review



### rating

Return review rating



### nickname

Return reviewer’s nickname



### email

Return reviewer’s email address



### title

Return review title



### body

Return review content



### sticky

Return whether the review is sticky/pinned



### status

Return review status



### created\_by

Return user ID of who created the review



### created\_at

Return creation timestamp of the review

{{ date-output-example created_at }}



### approved\_by

Return user ID of who approved the review



### approved\_at

Return approval timestamp of the review

{{ date-output-example approved_at }}



### product\_name

Return link of product with title



### product\_name\_string

Return product name



### product\_image

Return product image URL



### status\_tag

Return status tag/label for the review



### order\_id\_link

Return link to the related order



### customer\_email

Return customer email linked to the order



### medias

Return review media attachments (images/videos)



### is\_verified\_buyer

Return true or false whether reviewer is a verified buyer

