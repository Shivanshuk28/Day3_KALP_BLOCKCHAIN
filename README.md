# 🚀 Token Airdrop System on Kalp Blockchain

## Overview

This project implements a token airdrop system on the Kalp blockchain, consisting of:

1. A smart contract written in Go
2. A React frontend application using TypeScript

## Smart Contract Specifications

### Key Functions

1. `Initialize(name string, symbol string, decimals string) (bool, error)`
   - Sets up token metadata
   - Parameters: token name, symbol, and decimal places
   - Returns: success status and error (if any)

2. `Claim(amount int, address string) error`
   - Mints new tokens for users
   - Parameters: amount to mint, recipient address
   - Returns: error (if any)

3. `BalanceOf(account string) (int, error)`
   - Checks token balance of an account
   - Parameters: account address
   - Returns: balance and error (if any)

4. `TotalSupply() (int, error)`
   - Returns total tokens in circulation
   - Returns: total supply and error (if any)

5. `TransferFrom(from string, to string, value int) error`
   - Transfers tokens between accounts
   - Parameters: sender address, recipient address, amount
   - Returns: error (if any)

### Additional Functions

- `Name() (string, error)`: Returns token name
- `Symbol() (string, error)`: Returns token symbol

### Deployment Process

1. Sign up on [Kalp Studio Platform](https://doc.kalp.studio/Getting-started/Onboarding/How-to-Sign-Up-and-Log-In-to-Kalp-Studio-Platform/)
2. Navigate to Kalp Instant Deployer
3. Create a new smart contract:
   - Provide name, category, and description
   - Upload `smart-contract.zip` file
4. Deploy using [Kalp Instant Deployer](https://doc.kalp.studio/Dev-documentation/Kalp-DLT/Smart-Contract-Write-Test-Deploy-Interact/Deploy-the-smart-contract/)
5. Generate API endpoints for each function
6. Generate API key for authentication

## Frontend Application Specifications

### Technology Stack

- React with Next.js
- TypeScript
- Fetch API for network requests

### Key Components

1. `useKalpApi` Hook (`src/hooks/useKalpApi.ts`)
   - Manages API calls to the smart contract
   - Handles loading states and errors
   - Provides functions: claim, balanceOf, totalSupply, transferFrom

2. Main Application Component (`src/app/page.tsx`)
   - Implements user interface for interacting with the smart contract
   - Utilizes `useKalpApi` hook for blockchain interactions

### Setup and Configuration

1. Clone the repository
2. Navigate to `frontend` directory
3. Run `npm install` to install dependencies
4. Create `.env.local` file in the project root:
   ```
   NEXT_PUBLIC_API_KEY=your-kalp-api-key
   ```
5. Update API endpoints in `src/hooks/useKalpApi.ts`:
   - Replace placeholder URLs with actual endpoints from Kalp Studio
   - Example:
     ```typescript
     const claim = async (address: string) => {
       const endpoint = 'https://gateway-api.kalp.studio/v1/contract/kalp/invoke/YourContractID/Claim';
       // ... rest of the function
     };
     ```

### Running the Application

1. Start the development server:
   ```
   npm run dev
   ```
2. Open your browser and navigate to `http://localhost:3000`

### User Interface Features

The frontend should implement the following features:

1. Claim Tokens:
   - Input field for address
   - Button to trigger claim function

2. Check Balance:
   - Input field for account address
   - Display area for balance

3. Transfer Tokens:
   - Input fields for sender, recipient, and amount
   - Button to initiate transfer

4. Total Supply:
   - Display area for total token supply
   - Refresh button to update supply

5. Transaction History (Optional):
   - List of recent transactions
   - Details including addresses and amounts

### Error Handling and Loading States

- Implement loading indicators for API calls
- Display error messages for failed transactions
- Provide user feedback for successful operations

## Submission Requirements

1. Fully functional smart contract deployed on Kalp blockchain
2. Frontend application with all specified features implemented
3. Clean, well-documented code following best practices
4. Updated README with any additional setup or running instructions
5. Deployed frontend application with a live link
6. All API endpoints correctly configured and accessible

Extra features or improvements beyond the basic requirements are encouraged and will be considered positively in the evaluation.

For more detailed information on Kalp blockchain development, refer to the [Kalp SDK documentation](https://docs.kalp.studio/).
