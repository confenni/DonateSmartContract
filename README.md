# Smart Contract Server for Plugin Donate Crypto 

This server running in NodeJS with Hardhat configure for the smart contract system, in this server can running in local server or VPS. This server have a function for create smart contract with the deploy with Hardhat. Before the deploy new smart contract should be have a private account key (Etherium), network name, and url API key network.

## Installation

Download or Clone this repository. After that you open terminal in project and type command like bellow and enter, for install all package used.

```bash
npm install
```
    
## Running the server

The server can running if you type and enter

```bash
node scripts/index.js
```
## API Reference

#### Create Smart Contract

```http
  POST /createSmartContract
```

| Parameter             | Type     | Description                                     |
| :-------------------- | :------- | :---------------------------------------------- |
| `network`             | `string` | **Required**. Type of network                   |
| `url_api_key`         | `string` | **Required**. URL API KEY of network            |
| `private_key_account` | `string` | **Required**. Private Key Account from metamask |

If running this API endpoint, will be get result JSON like this
```json
{
    "status": true,
    "message": "Process Successfully",
    "data": {
        "address_contract": "0x71F3e30b1f00AD6201d4fBea7a223cB91B8f5614",
        "abi_json_url": "http://localhost:3000/abi_json/ABI_FILE_JSON_SMARTCONTRACT.json"
    }
}
```
## Tech Stack

**System:** NodeJS, Javascripts, ExpressJS, Hardhat
