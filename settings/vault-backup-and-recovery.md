---
description: This guide would describe the steps to set up Vaults backup and do recovery
---

# Vault Backup and Recovery

* Backup and recovery in PrimeVault require 3 organization admins, with any 2 admins able to recover the vaults together.
* To enable recovery in your workspace, first contact PrimeVault support and provide the email addresses of the three admins responsible for managing recovery. PrimeVault will then activate the recovery feature for your workspace. Once enabled, follow the steps below to complete the setup
* Each admin must create a secure password in their mobile app, download the encrypted backup file (zip) from the webapp, and store it safely.
* For recovery, 2 admins must provide both their passwords and encrypted backup files.

### Backup

#### 1. Setup Recovery Password in Mobile App

* If you're eligible for the backup and recovery process and haven't set up a recovery password yet, you'll see an option to do so on the homepage.

<figure><img src="../.gitbook/assets/image (2).png" alt="" width="188"><figcaption></figcaption></figure>

* Complete the password setup and keep it secure, as you'll need it for the recovery process.

#### 2. Download encrypted vault backup data

* After setting up the recovery password, the system will generate an encrypted backup file for you to download and store securely.
* This file will be required for recovery, so make sure to store it securely..
* In the Webapp, **Settings -> Vault Backup**, where you'll find the option to download the encrypted backup file.
* This encrypted backup file is unique to each admin involved in the backup and recovery process and must be downloaded and stored securely.
* You can download the encrypted file as many times as needed.
* When a new vault is added, the system automatically generates a new backup file, which you'll need to re-download and store securely.

<figure><img src="../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>

### Recovery

#### 1. Recreate Private Key

* Recovery is performed using a local offline tool provided by PrimeVault, [here](https://github.com/horcrux01/offline-recovery-tool-public). The readme in the GitHub has instructions to install the tool locally using the command line.

<figure><img src="../.gitbook/assets/image (4).png" alt="" width="375"><figcaption></figcaption></figure>

* Install the offline tool provided by PrimeVault on any machine.
* Any 2 out of the 3 users must upload their encrypted backup file and enter their recovery password.
* The local recovery tool will compute and return the private key in hex format for each vault across all supported chains.

#### 2. Create transaction to move funds

**For ECDSA-Based Blockchains (Ethereum, Polygon, Arbitrum, Optimism, etc.):**

* The recovery process provides you directly with a private key.&#x20;
* This key can be imported straight into MetaMask or other compatible wallets.&#x20;
* Once imported, you can easily create transactions within MetaMask to move your funds to the desired wallet.

**For EdDSA-Based Blockchains (Solana, Near, Aptos, Radix, ICP, etc.):**

* The recovery process does not yield a conventional private key
* Instead, PrimeVault provides a signing script to authorize transactions. You can use this script to sign any message, and by creating your own scripts based on it, you can move funds on these specific blockchains
* Contact PrimeVault for blockchain-specific scripts or assistance.
