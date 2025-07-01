# Editing a Policy Template

* Navigate to the **Policies** tab
* Find the template you want to edit
* Click on the **Edit** button next to the template
* Modify the template’s owners, viewers, or any attached policies
* Review your changes and compare them with the previous policies
* Submit the edit request
  * The request will follow the organization-level policy of collecting the quorum number of approvals. You can find this under the **Settings -> Admin Policies** tab
* Once approved, the changes will be applied to all the **Vaults** that use this template

{% hint style="info" %}
For each template, only one active edit request is allowed at a time. To create a new edit request, any existing one must be rejected if it is currently pending.
{% endhint %}

{% hint style="danger" %}
Please note that all transactions created before the policy change will follow the old policies. It might happen that the transaction can no longer meet quorum requirements for approval. If that happens, please reject the transaction and create a new one.
{% endhint %}

{% hint style="danger" %}
If an owner who previously created transactions is no longer part of the vault, all their pending transactions will be auto-declined if the edit request is approved.
{% endhint %}

{% embed url="https://www.loom.com/share/ad3a4df0eb354878a73dc85adf8c9d65?sid=bce5c78a-54bd-457e-8725-f3a8402ad975" %}
