# Foundry + thirdweb Smart Contract Development

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

This contract repository is pre-configured to build, test, and deploy smart contracts on the Electroneum Smart Chain using either Foundry tools or **thirdweb CLI**.

### thirdweb Deployment (Recommended)

thirdweb provides a secure, private-key-free contract deployment flow. Compiling and deploying is simple:

```shell
# Deploy your contract using thirdweb CLI
npx thirdweb deploy
```

This compiles your contracts and opens a web browser link to configure and deploy the contract directly onto the Electroneum Mainnet or Testnet through the thirdweb Dashboard.

---

### Foundry Tools Documentation

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Foundry Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Foundry Deploy

Deploy implementation and proxy contracts:

```shell
# Electroneum Testnet
forge script scripts/SellerPadiReceipt.s.sol:SellerPadiReceiptScript --rpc-url electroneum-testnet --account deployer --legacy --with-gas-price 10000000000 --broadcast --verify --verifier blockscout --verifier-url https://testnet-blockexplorer.electroneum.com/api
forge script scripts/SellerPadiShipment.s.sol:SellerPadiShipmentScript --rpc-url electroneum-testnet --account deployer --legacy --with-gas-price 10000000000 --broadcast --verify --verifier blockscout --verifier-url https://testnet-blockexplorer.electroneum.com/api

# Electroneum Mainnet
forge script scripts/SellerPadiReceipt.s.sol:SellerPadiReceiptScript --rpc-url electroneum --account myWallet --broadcast --verify --verifier blockscout --verifier-url https://blockexplorer.electroneum.com/api
forge script scripts/SellerPadiShipment.s.sol:SellerPadiShipmentScript --rpc-url electroneum --account myWallet --broadcast --verify --verifier blockscout --verifier-url https://blockexplorer.electroneum.com/api
```

---

## Deployed Contract Addresses

### Electroneum Mainnet (Chain ID `52014`)

- **SellerPadiReceipt (Digital Receipts) Proxy Address:** `0x8c82AAceD93B10FF9Bac51D67F54b01f54D7E4D6` (Verified)
- **SellerPadiReceipt Implementation:** `0x62F44CCef287476D4a343A92B00AC383e093f7C1` (Verified)
- **SellerPadiShipment (Delivery Verification) Proxy Address:** `0x4a8c44A709c83510D9236D672121bf3a0ca4Da3b` (Verified)
- **SellerPadiShipment Implementation:** `0x9a0fd40e4696Ba3aB72a2fB29e3836122d20E949` (Verified)

### Electroneum Testnet (Chain ID `5201420`)

- **SellerPadiReceipt (Digital Receipts) Proxy Address:** `0xdEd6b556A0f431CCd7085788f9adE5D5D442BcFE`
- **SellerPadiReceipt Implementation:** `0x24D810C8fDAeFba69a89347857DC794F67F8F440`
- **SellerPadiShipment (Delivery Verification) Proxy Address:** `0xFa332d7B5208f7f175EadB784618Ba0390262b7e`
- **SellerPadiShipment Implementation:** `0x6170f8bB1317232980448eE150d158bB6cC49301`
