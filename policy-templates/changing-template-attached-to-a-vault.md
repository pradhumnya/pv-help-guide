# Changing Template attached to a Vault

* Head over to the **Vaults** table
* Click on the **Edit** button next to a Vault
* Select the new template you want to be applied to the vault
* Proceed to the next page
* Compare the newly selected template with the existing one
* Submit the edit request
  * The request will follow the organization-level policy of collecting the quorum number of approvals. You can find this under the **Settings -> Admin Policies** tab
* Once approved, the Vault will start using the new template

{% hint style="info" %}
For each vault, only one active edit request is allowed at a time. To create a new edit request, any existing one must be rejected if it is currently pending.
{% endhint %}

{% hint style="danger" %}
Please note that all transactions created before the policy change will follow the old policies, and it might happen that the transaction can no longer meet the quorum number of approvals.
{% endhint %}

{% hint style="danger" %}
If an owner who previously created transactions is no longer part of the vault, all their pending transactions will be auto-declined if the edit request is approved.
{% endhint %}

{% embed url="https://www.loom.com/share/d19feedee7da425eb7a80bd261af5ea5?sid=04bc8d97-216b-4314-8e15-38163a0c2b50" %}
