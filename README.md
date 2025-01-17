![image](https://github.com/user-attachments/assets/3023d119-e795-4789-8f3c-78ff115e555c)


# Monad devnet phase - Contract Deployment

Monad is a high-performance Ethereum-compatible L1. Monad materially advances the efficient frontier in the tradeoff 

between decentralization and scalability.

## Step 1:  Fork this contract

## Step 2: Open Gitpod and log in with GitHub

## Step 3: Install the requirements 


 <code> nvm install 20 </code>

 <code> source /home/gitpod/.bashrc </code>

 <code> curl -L https://foundry.paradigm.xyz | bash </code>

 <code> foundryup </code>

 <code> wget -qO - 'https://proget.makedeb.org/debian-feeds/prebuilt-mpr.pub' | gpg --dearmor | sudo tee /usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg 1> /dev/null
  echo "deb [arch=all,$(dpkg --print-architecture) signed-by=/usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg] https://proget.makedeb.org prebuilt-mpr $(lsb_release -cs)" | sudo tee /etc/apt/sources.list.d/prebuilt-mpr.list
 </code>

 <code> sudo apt update </code>
 
 <code> sudo apt install just </code>

## Step 4: Create a file name 

 <code> forge init --template monad-developers/foundry-monad [File_name] </code>

 <code> cd [file_name] </code>

 <code> forge build </code>

## Step 5: Modify the foundry configuration

[profile.default]
src = "src"
out = "out"
libs = ["lib"]

Monad Configuration

eth-rpc-url = "[RPC_LINK]"

chain_id = 20143

Etherscan Configuration
[etherscan]

monadDevnet = { key = "DUMMY_VALUE", url = "[Explorer link]", chain = 20143 }

## Step 6: Run the contract 

 <code> forge compile </code>

 <code> forge create --private-key  --rpc-url [rpc_link] src/[file_path].sol:[filename] --broadcast </code>

 On successful deployment of smart contract, the output should be similar to the following:

Deployer: 0xB1aB62fdFC104512F594fCa0EF6ddd93FcEAF67b

Deployed to: 0x67329e4dc233512f06c16cF362EC3D44Cdc800e0

Transaction hash: 0xa0a40c299170c9077d321a93ec20c71e91b8aff54dd9fa33f08d6b61f8953ee0

## Step 7: Verify the contract

<code> forge verify-contract <contract_address> <contract_name> </code>

On successful verification of smart contract, you should get a similar output in your terminal:

Start verifying contract `0x1355a4f7829161a4d27BDb8970D32b89ef89A1Be`

Submitting verification for [src/Counter.sol:Counter] 0x1355a4f7829161a4d27BDb8970D32b89ef89A1Be.

Submitted contract for verification:

Response: `OK`

GUID: `1355a4f7829161a4d27bdb8970d32b89ef89a1be67448d78`
 
 

 


 

 

 

 
