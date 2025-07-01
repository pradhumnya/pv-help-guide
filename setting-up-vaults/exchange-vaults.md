# Exchange Vaults

**Exchange Vault Introduction**

* Connect your Exchange trading accounts in PrimeVault and provision necessary access controls to admins to move funds between Core Vaults and Exchanges
* Automate Vault-to-Exchange and Exchange-to-Exchange transfers
* **Note:** **Exchange Vault is a custodial Vault where the funds are in your Exchange’s custody**
* The Vault in PrimeVault provides a permissioned framework to interact with assets sitting on linked Exchanges and enables single-window administration of funds across Exchanges
* We’ve enabled connections to a large number of exchanges via our partner’s APIs (Mesh)

**How to use an Exchange Vault**

* Create an Exchange Vault
* Withdrawing assets out of Exchange Vault
* Depositing assets into Exchange Vault

### **Create an Exchange Vault**

1. Create API Key & Secret Key on your exchange’s platform (requirement varies as per exchange).  Explained in the next section for different exchanges.\

2. Complete steps as per the Exchange Vault flow. Select the policy template, review the assets and submit.

<figure><img src="https://lh7-us.googleusercontent.com/mCyoqu24XPISDTfbuYZTjuy6AXRay8iDtuxnh1S3xreVJ64vuimv75mA0EXHWoZ0erhHv71rNpwXp7SAx4ve1t1rcqpZ33pqmOOThh6hYoTrC4kQq0rf_8lf-CQrxiBDh6khoJm-55Q-00LAJ5UDEXU" alt=""><figcaption></figcaption></figure>

***



### API Key Setup for Exchanges

#### **Kraken**

`Settings` -> `API` -> `Create API Key`

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

* Kraken Help Center [link](https://support.kraken.com/hc/en-us/articles/360000919966-How-to-create-an-API-key)
* Permissions: Query, Deposit and Withdraw
* IPs for whitelisting: `13.59.176.125`, `18.223.183.241`
* Nonce window: 10000



#### Coinbase International

* `API` -> `Create API Key`

<figure><img src="../.gitbook/assets/image (49).png" alt="" width="563"><figcaption></figcaption></figure>

* Permissions -> `View` & `Transfer`
* IP Allowlist -> `54.151.154.241` and `18.136.156.129`

#### Coinbase Exchange

* API key setup similar as `Coinbase International` above.
* IP Allowlist -> `13.59.176.125` and `18.223.183.241`

#### Gateio

* Profile -> API Management -> Create API Key
* IPs to link: `13.59.176.125`, `18.223.183.241`
* Permissions
  * `Spot Trade` -> `Read Only`
  * `Wallet` -> `Read And Write`
  * `Withdraw` -> `Read And Write`
  * `Account` -> `Read And Write`

#### Mexc

`Profile` -> `API Management`

* Provide the permissions as below

<figure><img src="../.gitbook/assets/image (45).png" alt="" width="563"><figcaption></figcaption></figure>

* IPs to link: 13.59.176.125, 18.223.183.241

#### Binance

* `Profile` -> `Settings` -> `Account` -> `API Management`

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* IP Allowlist -> `54.151.154.241` and `18.136.156.129`
* Permissions
  * Enable Withdrawal

#### KuCoin

* `Profile` -> `API Management -> Create API Key`

<figure><img src="../.gitbook/assets/Screenshot 2025-01-08 at 4.08.20 PM.png" alt=""><figcaption></figcaption></figure>

* IP Allowlist -> `54.151.154.241` and `18.136.156.129`
* `Permissions`
  * `Withdrawal`

#### Bitget

`Profile` -> `API Key` -> `Create API Key`

* Enter name
* Permissions -> Read-write
* Permission type
  * Spot - Trade
  * Wallet - Transfer & Withdraw
* IP
  * 13.59.176.125, 18.223.183.241

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>



#### ByBit

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

IPs to whitelist

* `54.151.154.241` and `18.136.156.129`  (Comma separated and no space)

Permissions

* Assets
  * Account Transfer
  * Withdrawal



### **Withdrawing assets from Exchange Vault to Core Vault**

1. Whitelist core vault, other exchange vault and other addresses on the exchange using the specific exchange platform. This is a requirement to be able to withdraw funds from exchange account using PrimeVault.
2. In PrimeVault, to initiate transfer go to  `Transaction` -> `Transfer` and Select Exchange account, asset, chain, amount and counter party.
3. After all the inputs are provided, you will see the expected withdrawal fee computed based on the inputs.

<figure><img src="../.gitbook/assets/image (48).png" alt="" width="375"><figcaption></figcaption></figure>

***

### **Depositing Assets into Exchange Vault from Core Vault**

1. Use the PrimeVault platform to initiate deposits into the exchange

![](https://lh7-us.googleusercontent.com/ej44hrEFl9EQMuIQq91s3XwKQ_PZCiQDgFP2iakFLFLikDh1CsCEBit0naKt1RXgFc5hRjAZOG9FJ3eW7t1I30QCr6QqOE9vSl3R4VVV6m7-Pn8A2nwY41P4iHSSCYFEz5zP0wKRL5P9n159Nc7vvg4)

***

### Cross Exchange Transfer

* Cross-Exchange transfer would be similar to deposit and withdraw actions.&#x20;
* First, whitelist the destination exchange’s deposit address for withdrawals on the source exchange.&#x20;
* When you initiate a transfer in PrimeVault, it will trigger a withdrawal from the source exchange to the destination exchange’s (deposit)address.

###
