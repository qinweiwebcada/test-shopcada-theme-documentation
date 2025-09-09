# Gift Certificate

{% hint style="info" %}
**Email template**\
Use `gift_certificate` as the prefix when referencing variables in email templates.\
For example: `{{ gift_certificate.certificate_id }}`
{% endhint %}

### certificate\_id

Return gift certificate id



### name

Return gift certificate name



### currency

Return gift certificate currency



### customer\_id

Return gift certificate customer id



### issue\_amount

Return amount of gift certificate



### remaining\_amount

Return remaining amount of gift certificate



### created\_at

Return gift certificate purchase date

{{ date-output-example created_at }}



### expire\_at

Return gift certificate expiry date

{{ date-output-example expire_at }}



### is\_used

Return true or false if gift certificate is used



### is\_expired

Return true or false if gift certificate is expired



### info

Return [gift certificate information](liquid/variables/gift-certificate/gift-certificate-information.md) such as sender name, recipient name and others



&#x20;
