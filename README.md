# Send transactions to an EVM
## Moonbeam Test
Tests with a dev MoonBeam instance with the following parameters : <br/> 
``
docker run --rm --name moonbeam_development -p 9944:9944 -p 9933:9933 purestake/moonbeam:v0.20.0
--dev --ws-external --rpc-external --sealing 6000
``
<br/>
Sealing 6000 allows our node to generate automatically a new block every 6 secs.

## Deploy the contract
Deploy the smartcontract `stringStore.sol` to store strings on the EVM.

## Sending mass transactions
Sending mass transactions to the EVM with `transactions_sender.js`
### Setup
``
npm install
``
### Run the script
Update the config : contract address, user account in the init function and amount of transactions, amount of characters in the variable declaration and run it :
``
node transactions_sender.js
``

### Results
``
Success.
600 transactions (each storing 5000 caracters) have been done in parallel.
``