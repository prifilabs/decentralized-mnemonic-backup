#  Decentralized Mnemonic Backup System by PriFi Labs Inc.

## Project Description

> Not Your Keys, not Your Coins.

This crypto mantra, popularized by Andreas Antonopoulos, encourages us, crypto enthusiasts, to use non-custodial crypto wallets in which the private keys are directly stored on their device. However, using non-custodial wallets comes with the risk of losing all of our crypto assets if we lose our private keys. If our device gets lost, stolen or irremediably break down, our crypto assets might be locked forever. 

Fortunately, most non-custodial wallets such as Exodus (Bitcoin), Meta- mask (Ethereum) and Keplr (Secret Network) offer a way to recover our private keys by the mean of a “recovery phrase” also known as “mnemonic seed phrase”. It is the 12-word phrase that we are being given the first time we setup our wallet. Indeed, this mnemonic phrase is a really sensitive piece of information. Anyone who has access to this phrase would have full control over our crypto assets. Usually, it is recommended to write it down on a piece of paper and store it in a “safe place”. But where is that “safe place” exactly? In our physical wallet with our cash and credit cards? Not ideal as it could get lost or stolen. Inside our home? No ideal again as it could burn down. A safe deposit box in the vault of a bank? it might be the best solution after all but the logistics that comes with it makes that solution very cumbersome.

In the end, it is quite inconvenient to store physical objects safely. So, could we design a simple application that would take custody of my passphrase and would allow me to recover by simply using my email? Yes we could build such an application, it would be something similar to a password manager such as 1password for instance. However, such a solution requires 1) that the service provider is trustworthy an 2) that the whole application is se- cured. Indeed, such a centralized solution is not a good solution as it goes against the philosophy of decentralized application.

## Problem / Solution

In this paper, we propose a Decentralized Mnemonic Backup system that anyone can use to give custody to any blockchain passphrase to the Secret Network \cite{SecretNetwork} and recover it using a simple email. The idea is to encrypt the passphrase and split it into multiple Secret NFTs using the Shamir's Secret Sharing cryptographic protocol. The encryption key is saved in a Secret smart contract. This key is never recorded in any transaction. Instead, it is generated using the Diffie-Hellman Key Exchange Protocol that is similarly used in well known protocols such as TLS and Signal. 

## Detailed product description

All details of our solution is in [our whitepaper](https://github.com/prifilabs/decentralized-mnemonic-backup/raw/main/whitepaper/whitepaper.pdf).
 
## Go-to-Market plan

We plan to let people backing up their passphrase for free beyond paying the gas fee to register the encryption key and minting the Secret NFTs that embed the shares of the encrypting passphrase. However, we will generate revenue when users want to recover their mnemonic passphrase by paying a fee to retrieve the encryption key. 

## Value capture for Secret Network ecosystem

This backup system will demonstrate that the Secret Network privacy model is adequate to keep sensitive information confidential relying on two important features of Secret NFTs: secret metadata and private ownership.

Why implementing our backup system on Secret Network rather than Ethereum? Is it because Ethereum-based NFTs do not have secret metadata? Not really since we could have created a password protected version of the share and hid it inside a public NFT image using Steganography \cite{Steganography}. The real problem is that if an attacker knows that an NFT contains a share to recover a mnemonic phrase, he or she will be able to locate all others NFTs that contains the other shares easily since ownership is public on Ethereum. The fact that Secret NFTs protects the ownership is the key feature that makes our backup system secured. 

## Team members
* Thierry Sans: Founder, CEO of PriFi Labs Inc as well as an Associate Professor in Computer Science at University of Toronto
* David Liu: Co-Founder, CTO of PriFi Labs Inc as well as the CEO of dApp Technology Inc. with over 40 blockchain full stack developers
* Howe Gu: Advisor as well as the Head of Global Strategy, Customer Transformation & Innovation at Microsoft
* Kevin Oh: Blockchain full stack developer

## Team Website	

[PriFi Labs Inc.](https://prifi-labs.webflow.io/) 

## Team's experience
* Thierry Sans has 15 years experience in Academia. His expertise is computer security and data protection. 
* David Liu has built and managed over 30 blockchain projects. His expertise is Blockchain Full Stack development, Business Planning and execution.
* Howe Gu has worked and lead enterprise companies (PWC, Deloite, Microsoft) on Business Strategy, Customer Success and Business Consulting.
* Kevin Oh has...

We've been a team for 6 months.

## Team Code Reposs

[PriFi Labs on Github](https://github.com/prifilabs)

## Team LinkedIn Profiles

[Thierry Sans](https://www.linkedin.com/in/thierry-sans-0a281227/)
[David Liu](https://www.linkedin.com/in/davidzimingliu/)
[Howe Gu](https://www.linkedin.com/in/howegu/)

## Development Roadmap

We will require 3 months to complete this project. We intend to hav 2 developers full-time at a total cost of $100,000.

Example milestones:

* smart contract: 40k
* mailer backend: 30k
* frontend deployed on IPFS fully integrated with secret contract and mailer backend: 30k
* documentation: 10k

Ideally, we can receive payments in 3 disbursements, one at the beginning of the grant, one after implementation of the smart contract and last payment when the development work is completed.

We would be willing to consider part payment in SCRTs. 

## Additional Information
N/A.
