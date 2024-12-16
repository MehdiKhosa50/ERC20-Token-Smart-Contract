# MyToken (MTK) Smart Contract

A sophisticated ERC20 token implementation with enhanced functionality including pausability, burning mechanism, permit features, and upgradeability.

## Features

- 🔐 Upgradeable using UUPS pattern
- ⏸️ Pausable transfers
- 🔥 Token burning capability
- ✍️ ERC20 Permit functionality
- 👑 Owner-controlled minting
- 🔒 OpenZeppelin secure implementation

## Technical Details

- Built with Solidity ^0.8.20
- Implements multiple OpenZeppelin upgradeable contracts
- Uses initializer pattern for proxy deployment

## Contract Functions

### Administrative Functions

- `initialize(address initialOwner)`: Sets up the token with initial parameters
- `pause()`: Pauses all token transfers (owner only)
- `unpause()`: Resumes token transfers (owner only)
- `mint(address to, uint256 amount)`: Creates new tokens (owner only)

### Token Information

- Name: "MyToken"
- Symbol: "MTK"
- Decimals: 18 (default)

## Dependencies

This contract relies on the following OpenZeppelin contracts:
- ERC20Upgradeable
- ERC20BurnableUpgradeable
- ERC20PausableUpgradeable
- OwnableUpgradeable
- ERC20PermitUpgradeable
- Initializable
- UUPSUpgradeable

## Installation

```bash
npm install @openzeppelin/contracts-upgradeable

Deployment
Deploy the implementation contract
Deploy the proxy contract pointing to the implementation
Initialize the proxy with the desired owner address
Security
Contract inherits from well-audited OpenZeppelin contracts
Includes access control mechanisms
Upgradeable architecture allows for future improvements
Constructor is disabled to prevent implementation contract initialization
License
This project is licensed under the MIT License - see the LICENSE file for details

Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Audit Status
⚠️ This contract has not been audited. Use at your own risk.
