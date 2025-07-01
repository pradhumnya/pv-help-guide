# Gas Vaults

**Gas Vault Introduction**

A gas vault is a non-custodial “gas tank” that is configured by default to monitor gas token balance in each Core Vault (on all chains) and automatically replenishes a vault when token balance falls below threshold

**Steps to set up a Gas Vault**

* Create a Gas Vault&#x20;
* Automating a Gas Vault&#x20;
* Funding a Gas Vault

### Create a Gas Vault

1. Select ‘+New Vault’ from the right side of the platform

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

2. Name your Gas Vault and select ‘Gas Vault’ under Vault Type

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

3.  Add Vault Owners and Viewers (optional)

    1. **Vault Owner:** Owners can transfer funds, within specified limits, from this vault to top up any Core Vault with supported gas tokens
    2. **Viewer:** A Viewer can view a Vault, its balances, any pending and processed processed transactions, and more but not create or transactions from the Vault.

    <figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>
4. Set transfer limit policies to specify spend limits for vault owners to move assets from gas vault to other vaults. This flow is similar to setting up policies in [core vault ](core-vaults.md#set-up-vault-policies)

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

5. Review and finish

***

### Automating a Gas Vault

1. PrimeVault's gas vault can monitor the gas token balance in each Core Vault (on all chains) and automatically replenish a vault when the token balance falls below the threshold
2. Instead of manually replenishing each vault's chain with native gas token, use the gas vault automation under 'Settings' to automate the process&#x20;

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

3.  Select the Gas Vault which you would like to setup an automation and click on '+ Add Automated Refill' and follow these steps

    1. Select the chain where you would like to automate refilling of gas
    2. Select the vaults where you would like to automate refilling of gas (you can select multiple)
    3. Enter the refill trigger balance - Refill will trigger when core vaults' balance falls below the entered number
    4. Enter the refill amount - The amount that will be refilled for the vaults chain on hitting the trigger\


    <figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

***

### Funding a Gas Vault

**Fund gas vault with USDT on Polygon (support for USDC soon) for the following chains**

| Chain    | Min Gas Token Balance (Trigger) | Refill Amount |
| -------- | ------------------------------- | ------------- |
| Ethereum | 0.01 ETH                        | 0.1 ETH       |
| Optimism | 0.005 OETH                      | 0.1 OETH      |
| Polygon  | 0.05 MATIC                      | 10 MATIC      |
| Arbitrum | 0.005 AETH                      | 0.1 AETH      |

**Fund gas vault with native chain assets for the following chains. Support for stablecoin-based funding coming to all chains soon.**

| Chain  | Min Gas Token Balance (Trigger) | Refill Amount |
| ------ | ------------------------------- | ------------- |
| Solana | 0.005 SOL                       | 0.1 SOL       |
| Aptos  | 0.005 APT                       | 0.1 APT       |

**Upcoming support for:**

| Chain   | Min Gas Token Balance (Trigger) | Refill Amount |
| ------- | ------------------------------- | ------------- |
| Near    | 0.003 NEAR                      | 0.01 NEAR     |
| Bitcoin | <p><br></p>                     | <p><br></p>   |
