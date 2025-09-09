# Store Credit

{% hint style="info" %}
**Email template**\
Use `storecredit` as the prefix when referencing variables in email templates.\
For example: `{{ storecredit.credit_id }}`
{% endhint %}

### credit\_id

Return ID of store credit



### name

Return store credit name



### currency

Return store credit currency



### customer\_id

Return store credit customer ID



### issue\_amount

Return store credit amount



### remaining\_amount

Return remaining amount of store credit



### created\_at

Return the date of store credit gained

{{ date-output-example created_at }}



### valid\_from

Return the valid date of store credit

{{ date-output-example valid_from }}



### expire\_at

Return expiry date of store credit

{{ date-output-example expire_at }}



### remarks

Return remarks of store credit



### is\_used

Return true or false if store credit is used



### is\_expired

Return true or false if store credit is expired

