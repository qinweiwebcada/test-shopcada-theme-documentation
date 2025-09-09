# Invite

{% hint style="info" %}
**Email template**\
Use `invite` as the prefix when referencing variables in email templates.\
For example: `{{ invite.invitation_code }}`
{% endhint %}

### invitation\_code

Return invitation code in string



### inviter\_customer\_id

Return inviter ID



### invitee\_email

Return email of invitee



### invited\_at

Return date of invitation sent



### expire\_at

Return expiry date of the invitation

{{ date-output-example expire_at }}



### joined\_at

Return date of invitee accept the invitation

{{ date-output-example joined_at }}



### invitee\_customer\_id

Return invitee ID



### status

Return true or false if invite is accepted

