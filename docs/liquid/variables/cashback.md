# Cashback

{% hint style="info" %}
**Email template**\
Use `cashback` as the prefix when referencing variables in email templates.\
For example: `{{ cashback.cashback_id }}`
{% endhint %}

### cashback\_id

Return ID of cashback&#x20;



### order\_id

Return cashback order ID



### cashback.name

Return cashback name



### currency

Return cashback currency



### customer\_id

Return cashback customer ID



### issue\_amount

Return cashback amount



### remaining\_amount

Return cashback remaining amount



### created\_at

Return cashback created date

{{ date-output-example created_at }}



### expire\_at

Return cashback expire date

{{ date-output-example expire_at }}



### remarks

Return cashback admin notes



### is\_expired

Return true or false if cashback is expired



### is\_used

Return true or false if cashback is used

