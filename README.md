# TrustChain Escrow

A decentralized escrow application on Ethereum. A buyer locks funds in a smart contract, the seller delivers, and funds are released only when the agreed conditions are met. Disputes can be raised and resolved by an arbiter, removing the need to trust a middleman.

## **1. How It Works**

1. Buyer creates an escrow with the seller address, arbiter address and amount
2. Buyer deposits ETH into the contract
3. Seller delivers the goods or service
4. Buyer confirms delivery and funds are released to the seller
5. If there is a dispute, the arbiter decides to release or refund

## **2. Tech Stack**

| Layer | Technology |
|---|---|
| Smart contract | Solidity |
| Frontend | React |
| Web3 library | Ethers.js |
| Wallet | MetaMask |
| Network | Sepolia testnet |

## **3. Contract Overview**

| Function | Caller | Purpose |
|---|---|---|
| `createEscrow` | Buyer | Open a new escrow agreement |
| `deposit` | Buyer | Lock funds in the contract |
| `confirmDelivery` | Buyer | Release funds to the seller |
| `raiseDispute` | Buyer or seller | Flag the escrow for arbitration |
| `resolveDispute` | Arbiter | Release to seller or refund buyer |

## **4. Getting Started**

```bash
git clone https://github.com/devmoeez/trustchain-escrow.git
cd trustchain-escrow
npm install
npm start
```

Connect MetaMask to Sepolia and fund your wallet from a Sepolia faucet before testing.

## **5. Security Notes**

- Checks-effects-interactions pattern on all fund transfers
- Role checks on every state-changing function
- Testnet only; not audited for mainnet use

## **6. Author**

**Moeez Hashmi**
