# Automated Reward

{% hint style="info" %}
**Email template**\
Use `automated_reward` as the prefix when referencing variables in email templates.\
For example: `{{ automated_reward.ewid }}`
{% endhint %}

### ewid

Return automated reward ID



### title

Return automated reward title



### effective\_start

Return effective start date

{{ date-output-example effective_start }}


### effective\_end

Return effective end date

{{ date-output-example effective_end }}



### earning\_limit\_time

Return earning limit time set



### earning\_limit\_period

Return earning limit period, by hour, day, week, month or year



### site\_earning\_limit\_time

Return site wide earning limit time set



### delay\_interval

Return the delay interval per day for user to claim this point again



### created\_at

Return automated reward creation date

{{ date-output-example created_at }}



### changed\_at

Return automated reward change date

{{ date-output-example changed_at }}



### send\_email

Return type of email sending



### action\_type

Return type of action to perform



### action\_value

Return action value based on action type



