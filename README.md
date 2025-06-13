# ⏳ Time Locked Vault

A decentralized application that allows users to create time-locked vaults for their ETH. Users can deposit ETH and specify a lock duration, after which they can withdraw their funds.

## 🔑 Key Features

- Create multiple time-locked vaults
- Deposit any amount of ETH
- Set custom lock durations (minimum 1 minute)
- Full or partial withdrawals after lock period
- View all your vaults and their status
- Extend lock duration (owner only)

## 🛠 Tech Stack

- Solidity (Smart Contract)
- Hardhat (Development Environment)
- React (Frontend)
- ethers.js (Blockchain Interaction)
- MetaMask (Wallet Connection)

## 📦 Installation

1. Clone the repository:
```bash
git clone [your-repo-url]
cd time-locked-vault
```

2. Install dependencies:
```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd time-locked-vault-frontend
npm install
```

3. Create a `.env` file in the root directory:
```env
PRIVATE_KEY=your_private_key
ETHERSCAN_API_KEY=your_etherscan_api_key
```

## 🚀 Usage

1. Start local blockchain:
```bash
npx hardhat node
```

2. Deploy contract:
```bash
npx hardhat run scripts/deploy.js --network localhost
```

3. Start frontend:
```bash
cd time-locked-vault-frontend
npm run dev
```

## 💼 Smart Contract Functions

- `deposit(uint _lockDurationInSeconds)`: Create a new vault with specified lock duration
- `withdraw(uint _vaultIndex)`: Withdraw all funds from a vault after lock period
- `partialWithdraw(uint _vaultIndex, uint _amount)`: Withdraw specific amount from a vault
- `getVaults(address _user)`: View all vaults for a specific user
- `isUnlocked(uint _vaultIndex)`: Check if a vault's lock period has expired
- `getTimer(uint _vaultIndex)`: Get remaining lock time for a vault

## 🔒 Security Features

- Re-entrancy protection
- Minimum lock time enforcement
- Owner-only functions
- Safe withdrawal pattern

## 🧪 Testing

Run the test suite:
```bash
npx hardhat test
```

## 📝 License

This project is licensed under the MIT License.
