# 🚀 Guide: Deploying TipJar Smart Contract on Base Using Remix

This guide explains how to deploy and interact with a **TipJar smart contract** on the **Base network** using Remix IDE.  

---

## 📌 Prerequisites
- A **MetaMask wallet** installed in your browser or mobile device.  
- Some **ETH bridged to Base** (either on Base Mainnet or Base Sepolia testnet).  
- Access to [Remix IDE](https://remix.ethereum.org/).  

---

## ⚙️ Step 1 – Open Remix
1. Visit **Remix IDE** in your browser.  
2. Create a new file and paste the TipJar smart contract code.  
3. Save the file with a `.sol` extension (for example: `TipJar.sol`).  

---

## ⚙️ Step 2 – Compile the Contract
1. In the left panel, open the **Solidity Compiler** tab.  
2. Select **compiler version 0.8.30**.  
3. Enable optimization (recommended: Runs = 200).  
4. Click the **Compile** button.  

---

## ⚙️ Step 3 – Deploy on Base
1. Switch MetaMask to **Base Mainnet** or **Base Sepolia**.  
2. In Remix, open the **Deploy & Run Transactions** tab.  
3. Under **Environment**, select **Injected Provider - MetaMask**.  
4. Choose the `TipJar` contract from the dropdown.  
5. Click **Deploy** and confirm the transaction in MetaMask.  

---

## ⚙️ Step 4 – Verify on BaseScan
1. Copy your deployed contract address from Remix.  
2. Open [BaseScan](https://basescan.org/) (or [BaseScan Sepolia](https://sepolia.basescan.org/) if you used testnet).  
3. Paste your contract address in the search bar.  
4. Click **Verify and Publish**.  
5. Select the correct settings:  
   - Compiler: 0.8.30  
   - License: MIT  
   - Optimization: Enabled (Runs = 200 if used during compilation)  
6. Paste your contract code into the editor.  
7. Click **Verify**.  

---

## ⚙️ Step 5 – Interact with the Contract
- **Donate with a message**:  
  Use the `donate` function in Remix. Enter a message in quotes (e.g., `"Hello"`), specify an ETH value (e.g., `0.001 ether`), then click **transact**.  

- **Donate without a message**:  
  Send ETH directly to the contract address using MetaMask. The contract will automatically record the donation with a default message.  

- **Withdraw**:  
  Only the contract owner can call the `withdraw` function. This transfers all ETH stored in the contract to the owner’s wallet.  

---

## ✅ Notes
- Always test on **Base Sepolia testnet** before deploying on **Base Mainnet**.  
- Donations and withdrawals are visible on **BaseScan** under the **Events** tab.  
- This guide can be included in your repository to help others replicate the deployment.  



