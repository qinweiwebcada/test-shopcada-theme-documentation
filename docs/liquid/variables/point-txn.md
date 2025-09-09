# Point Transaction

{% hint style="info" %}
**Email template**\
Use `point_txn` as the prefix when referencing variables in email templates.\
For example: `{{ point_txn.txn_id }}`
{% endhint %}

### txn\_id

Return point ID



### customer\_id

Return customer ID of the point



### points

Return points



### created\_at

Return date of the point gained

{{ date-output-example created_at }}



### expire\_at

Return expiry date of the point

{{ date-output-example expire_at }}



### order\_id

Return order ID of the point



### operation

Return operation method to gain the point



### description

Return description of the point



### entity\_type

Return entity type of the point



### entity\_id

Return entity ID of the point

