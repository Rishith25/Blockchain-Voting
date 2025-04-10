# Blockchain Voting System

This project is a decentralized voting application built on the Ethereum blockchain. It allows users to cast votes securely and transparently, leveraging smart contracts for vote management.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Running the Application](#running-the-application)
- [Interacting with the DApp](#interacting-with-the-dapp)
- [Testing](#testing)
- [License](#license)

## Overview

The Blockchain Voting System consists of:

1. **Smart Contracts**: Written in Solidity (`Election.sol`), these contracts manage the election process, including candidate registration and vote tallying.
2. **Frontend Interface**: A web-based interface (`index.html`) that allows users to interact with the smart contract, view candidates, and cast votes.
3. **Backend Integration**: Utilizes Web3.js (`app.js`) to connect the frontend with the Ethereum blockchain.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- [Node.js](https://nodejs.org/en/download/)
- [Truffle Suite](https://trufflesuite.com/docs/truffle/getting-started/installation/)
- [Ganache](https://trufflesuite.com/ganache/) (for local Ethereum blockchain simulation)
- [MetaMask](https://metamask.io/) browser extension (for managing Ethereum accounts)

## Project Structure

The repository contains the following directories and files:

- `contracts/`: Contains Solidity smart contracts.
  - `Election.sol`: The main smart contract for the voting system.
- `migrations/`: Deployment scripts for migrating contracts to the blockchain.
- `src/`: Frontend files.
  - `index.html`: The main HTML file for the user interface.
  - `js/`: JavaScript files.
    - `app.js`: Handles interaction between the frontend and smart contracts.
    - `bootstrap.min.js`: Bootstrap framework for styling.
    - `jquery.min.js`: jQuery library for DOM manipulation.
    - `truffle-contract.js`: Truffle's contract abstraction for JavaScript.
    - `web3.min.js`: Web3.js library for blockchain interaction.
  - `css/`: Stylesheets.
    - `bootstrap.min.css`: Bootstrap CSS.
    - `styles.css`: Custom styles for the application.
- `test/`: Contains test scripts for the smart contracts.
- `truffle-config.js`: Configuration file for Truffle.
- `package.json`: Node.js project dependencies.

## Setup and Installation

1. **Clone the Repository**:

  ```bash
   git clone https://github.com/Rishith25/Blockchain-Voting.git
   ```

2. **Navigate to the Project Directory**:

  ```bash
  cd Blockchain-Voting
  ```
3. Install Dependencies:

  ```bash
  npm install
  ```

4. Start Ganache:

- Open Ganache and start a new workspace. This will simulate a local Ethereum blockchain for development and testing.

5. Compile the Smart Contracts:

  ```bash
  truffle compile
  ```

6. Migrate the Smart Contracts to the Blockchain:

  ```bash
  truffle migrate
  ```

## Running the Application

1. Start the Development Server:

- The project uses lite-server to serve the frontend files. Start the server with:

  ```bash
  npm run dev
  ```

  This will open the application in your default web browser.

2. Connect MetaMask to the Local Blockchain:

- Open MetaMask and create/import an account.

- Connect MetaMask to the local blockchain provided by Ganache by adding a custom RPC network with the URL http://127.0.0.1:7545.

## Interacting with the DApp

- Viewing Candidates: The homepage displays a list of candidates retrieved from the smart contract.

- Casting a Vote:

  - Select a candidate from the dropdown menu.

  - Click the "Vote" button.

  - Confirm the transaction in MetaMask.

- Vote Tally: After voting, the total votes for each candidate will update accordingly.

## Testing

To run the tests for the smart contracts:

  ```bash
  truffle test
  ```

  This will execute the test scripts located in the test/ directory.
 
