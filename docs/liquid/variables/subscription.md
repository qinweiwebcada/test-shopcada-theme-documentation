# Subscription

{% hint style="info" %}
**Email template**\
Use `subscription` as the prefix when referencing variables in email templates.\
For example: `{{ subscription.subscription_id }}`
{% endhint %}

### subscription\_id

Return subscription ID



### uid

Return user ID



### occurence

Return occurrence count



### order\_id

Return related order ID



### created\_at

Return subscription creation timestamp

{{ date-output-example created_at }}



### start\_at

Return subscription start timestamp

{{ date-output-example start_at }}



### last\_occur\_at

Return last occurrence timestamp

{{ date-output-example last_occur_at }}



### next\_schedule\_at

Return next scheduled occurrence timestamp

{{ date-output-example next_schedule_at }}



### frequency\_range

Return frequency range of subscription



### frequency

Return subscription frequency



### max\_occurrence

Return maximum allowed occurrences



### min\_occurrence

Return minimum required occurrences



### nid

Return product ID



### model

Return product model/SKU



### qty

Return quantity of product in the subscription



### shipping\_address\_id

Return shipping address ID



### shipping\_address

Return shipping address details



### formatted\_shipping\_address

Return formatted shipping address (for display)



### billing\_address\_id

Return billing address ID



### billing\_address

Return billing address details



### status

Return subscription status



### remark

Return remarks or notes on the subscription



### subscription\_product\_id

Return subscription product ID



### terminate\_reason

Return termination reason



### terminate\_at

Return termination timestamp

{{ date-output-example terminate_at }}



### detail\_url

Return URL to subscription details page



### status\_tag

Return status tag/label for the subscription



### product

Return product details



### product\_link

Return product title link



### replenishment\_cycle

Return replenishment cycle description



### subscription\_product

Return subscription product details



### subscription\_price

Return subscription price



### skip\_url

Return URL to skip the next occurrence



### reschedule\_url

Return URL to reschedule the next occurrence



### pause\_url

Return URL to pause the subscription



### resume\_url

Return URL to resume a paused subscription



### terminate\_url

Return URL to terminate the subscription



### update\_address\_url

Return URL to update shipping address



### manage\_subscription\_url

Return URL to manage subscription overview



### subscription\_pre\_remind\_day

Return number of days before occurrence to send reminder



### subscription\_payment\_fail\_remind\_day

Return number of days before payment retry reminder



### status\_text

Return subscription status as text



### order

Return related order details



### allow\_termination

Return true or false whether the subscription can be terminated

