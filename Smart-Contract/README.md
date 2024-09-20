# 🚀 Token Airdrop Smart Contract on Kalp Blockchain

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Smart Contract Specifications](#smart-contract-specifications)
4. [Setup and Installation](#setup-and-installation)
5. [Deploying the Smart Contract](#deploying-the-smart-contract)
6. [Interacting with the Smart Contract](#interacting-with-the-smart-contract)
7. [Testing](#testing)
8. [Troubleshooting](#troubleshooting)
9. [Additional Resources](#additional-resources)

## Overview

This project implements a token airdrop system using a smart contract on the Kalp blockchain. The smart contract, written in Go, manages the distribution of fungible tokens, allowing users to claim tokens through an airdrop mechanism.

## Prerequisites

- Go version `>=1.19` but `<1.20`
- Kalp Studio account
- Basic understanding of blockchain concepts and Go programming

## Smart Contract Specifications

### Key Functions

1. `Initialize(name string, symbol string, decimals string) (bool, error)`
   - Purpose: Sets up initial token metadata
   - Parameters:
     - `name`: Human-readable name of the token (e.g., "Kalp Token")
     - `symbol`: Short identifier for the token (e.g., "KLP")
     - `decimals`: Number of decimal places for token amounts
   - Returns: Success status (bool) and error (if any)

2. `Claim(amount int, address string) error`
   - Purpose: Mints new tokens and assigns them to a specified address
   - Parameters:
     - `amount`: Number of tokens to mint
     - `address`: Recipient's blockchain address
   - Returns: Error (if any)

3. `BalanceOf(account string) (int, error)`
   - Purpose: Retrieves the token balance of a given account
   - Parameters:
     - `account`: Address to check balance for
   - Returns: Balance (int) and error (if any)

4. `TotalSupply() (int, error)`
   - Purpose: Returns the total number of tokens in circulation
   - Returns: Total supply (int) and error (if any)

5. `TransferFrom(from string, to string, value int) error`
   - Purpose: Transfers tokens from one account to another
   - Parameters:
     - `from`: Sender's address
     - `to`: Recipient's address
     - `value`: Amount of tokens to transfer
   - Returns: Error (if any)

### Additional Functions

- `Name() (string, error)`: Returns the name of the token
- `Symbol() (string, error)`: Returns the symbol of the token

## Setup and Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Build-Hackathon/junior.git
   ```

2. Navigate to the smart contract directory:
   ```sh
   cd junior/airdrop-vending-machine/smart-contract
   ```

3. Install dependencies:
   ```sh
   go mod tidy
   ```

4. Verify the folder structure:
   ```
   airdrop-vending-machine
   ├── smart-contract
   │   ├── vendor
   │   ├── go.mod
   │   ├── go.sum
   │   ├── main.go
   │   └── krc.go  (Your Airdrop Vending Machine contract file)
   ```

## Deploying the Smart Contract

1. Sign up and log in to [Kalp Studio Platform](https://doc.kalp.studio/Getting-started/Onboarding/How-to-Sign-Up-and-Log-In-to-Kalp-Studio-Platform/)

2. Navigate to Kalp Instant Deployer in the dashboard

3. Create a new smart contract:
   - Click "Create New" Smart Contract
   - Fill in the details:
     - Name: Choose a name for your contract
     - Category: Select appropriate category
     - Description: Briefly describe your contract's purpose
   - Upload the `smart-contract.zip` file containing your Go code

4. Deploy the contract using the Kalp Instant Deployer

5. After deployment, Kalp Studio will provide:
   - API endpoints for each function in your contract
   - Options to generate an API key for authentication

## Interacting with the Smart Contract

Use Postman or a similar API testing tool to interact with your deployed smart contract. Here's a guide for each main function:

### 1. Initialize the Contract

- **Method:** POST
- **URL:** `https://your-api-endpoint/Initialize`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "name": "KalpToken",
    "symbol": "KALP",
    "decimals": "2"
  }
  ```

### 2. Claim Tokens

- **Method:** POST
- **URL:** `https://your-api-endpoint/Claim`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "amount": 1000,
    "address": "user-address"
  }
  ```

### 3. Check Balance

- **Method:** GET
- **URL:** `https://your-api-endpoint/BalanceOf?account=user-address`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio

### 4. Transfer Tokens

- **Method:** POST
- **URL:** `https://your-api-endpoint/TransferFrom`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "from": "user-address",
    "to": "recipient-address",
    "value": 500
  }
  ```

## Testing

1. Write unit tests for each function in your smart contract
2. Use Go's testing framework to run tests locally before deployment
3. Test edge cases and error handling scenarios
4. Ensure proper authorization checks are in place

Example test structure:

```go
func TestInitialize(t *testing.T) {
    //

# Clicked Code Block to apply Changes From

# 🚀 Token Airdrop Smart Contract on Kalp Blockchain

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Smart Contract Specifications](#smart-contract-specifications)
4. [Setup and Installation](#setup-and-installation)
5. [Deploying the Smart Contract](#deploying-the-smart-contract)
6. [Interacting with the Smart Contract](#interacting-with-the-smart-contract)
7. [Testing](#testing)
8. [Troubleshooting](#troubleshooting)
9. [Additional Resources](#additional-resources)

## Overview

This project implements a token airdrop system using a smart contract on the Kalp blockchain. The smart contract, written in Go, manages the distribution of fungible tokens, allowing users to claim tokens through an airdrop mechanism.

## Prerequisites

- Go version `>=1.19` but `<1.20`
- Kalp Studio account
- Basic understanding of blockchain concepts and Go programming

## Smart Contract Specifications

### Key Functions

1. `Initialize(name string, symbol string, decimals string) (bool, error)`
   - Purpose: Sets up initial token metadata
   - Parameters:
     - `name`: Human-readable name of the token (e.g., "Kalp Token")
     - `symbol`: Short identifier for the token (e.g., "KLP")
     - `decimals`: Number of decimal places for token amounts
   - Returns: Success status (bool) and error (if any)

2. `Claim(amount int, address string) error`
   - Purpose: Mints new tokens and assigns them to a specified address
   - Parameters:
     - `amount`: Number of tokens to mint
     - `address`: Recipients blockchain address
   - Returns: Error (if any)

3. `BalanceOf(account string) (int, error)`
   - Purpose: Retrieves the token balance of a given account
   - Parameters:
     - `account`: Address to check balance for
   - Returns: Balance (int) and error (if any)

4. `TotalSupply() (int, error)`
   - Purpose: Returns the total number of tokens in circulation
   - Returns: Total supply (int) and error (if any)

5. `TransferFrom(from string, to string, value int) error`
   - Purpose: Transfers tokens from one account to another
   - Parameters:
     - `from`: Senders address
     - `to`: Recipients address
     - `value`: Amount of tokens to transfer
   - Returns: Error (if any)

### Additional Functions

- `Name() (string, error)`: Returns the name of the token
- `Symbol() (string, error)`: Returns the symbol of the token

## Setup and Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Build-Hackathon/junior.git
   ```

2. Navigate to the smart contract directory:
   ```sh
   cd junior/airdrop-vending-machine/smart-contract
   ```

3. Install dependencies:
   ```sh
   go mod tidy
   ```

4. Verify the folder structure:
   ```
   airdrop-vending-machine
   ├── smart-contract
   │   ├── vendor
   │   ├── go.mod
   │   ├── go.sum
   │   ├── main.go
   │   └── krc.go  (Your Airdrop Vending Machine contract file)
   ```

## Deploying the Smart Contract

1. Sign up and log in to [Kalp Studio Platform](https://doc.kalp.studio/Getting-started/Onboarding/How-to-Sign-Up-and-Log-In-to-Kalp-Studio-Platform/)

2. Navigate to Kalp Instant Deployer in the dashboard

3. Create a new smart contract:
   - Click "Create New" Smart Contract
   - Fill in the details:
     - Name: Choose a name for your contract
     - Category: Select appropriate category
     - Description: Briefly describe your contract's purpose
   - Upload the `smart-contract.zip` file containing your Go code

4. Deploy the contract using the Kalp Instant Deployer

5. After deployment, Kalp Studio will provide:
   - API endpoints for each function in your contract
   - Options to generate an API key for authentication

## Interacting with the Smart Contract

Use Postman or a similar API testing tool to interact with your deployed smart contract. Here's a guide for each main function:

### 1. Initialize the Contract

- **Method:** POST
- **URL:** `https://your-api-endpoint/Initialize`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "name": "KalpToken"
    "symbol": "KALP"
    "decimals": "2"
  }
  ```

### 2. Claim Tokens

- **Method:** POST
- **URL:** `https://your-api-endpoint/Claim`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "amount": 1000,
    "address": "user-address"
  }
  ```

### 3. Check Balance

- **Method:** GET
- **URL:** `https://your-api-endpoint/BalanceOf?account=user-address`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio

### 4. Transfer Tokens

- **Method:** POST
- **URL:** `https://your-api-endpoint/TransferFrom`
- **Headers:**
  - `x-api`: Your API key from Kalp Studio
- **Body (raw JSON):**
  ```json
  {
    "from": "user-address"
    "to": "recipient-address"
    "value": 500
  }
  ```

## Testing

1. Write unit tests for each function in your smart contract
2. Use Go's testing framework to run tests locally before deployment
3. Test edge cases and error handling scenarios
4. Ensure proper authorization checks are in place

Example test structure:

</rewritten_file>
