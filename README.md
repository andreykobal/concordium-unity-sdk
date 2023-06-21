# Concordium Unity SDK Documentation
===============================

**Concordium Unity SDK**
The Concordium Unity SDK provides developers with the tools and functionalities to interact with the Concordium blockchain within a Unity environment. This documentation outlines the classes, methods, and features available in the SDK.

**Classes and Methods**

**ConcordiumSDK Class:**
Description: The ConcordiumSDK class serves as the entry point for interacting with the Concordium blockchain within a Unity environment.

Methods:
- Initialize()
  Description: Initializes the Concordium SDK by establishing a connection with the Concordium blockchain network.
  Parameters: None.

- CreateAccount(password)
  Description: Generates a new account by creating account keys and storing them securely. Returns the newly created account object.
  Parameters:
    - password (string): The password to encrypt the account data.

- ImportAccount(accountData, password)
  Description: Imports an existing account by decrypting and verifying the account data provided. Returns the imported account object.
  Parameters:
    - accountData (string): The encrypted account data to be imported.
    - password (string): The password to decrypt the account data.

- GetAccountBalance(account)
  Description: Retrieves the balance of the specified account from the Concordium blockchain.
  Parameters:
    - account (Account): The account object for which to retrieve the balance.

- SendTransaction(senderAccount, recipientAddress, amount)
  Description: Constructs and submits a transaction to send a specified amount from the sender's account to the recipient's address.
  Parameters:
    - senderAccount (Account): The sender's account object.
    - recipientAddress (string): The recipient's address.
    - amount (decimal): The amount to be sent in the transaction.

**AccountManager Class:**
Description: The AccountManager class handles account creation, import, and secure storage functionalities within the Concordium Unity SDK.

Methods:
- GenerateKeys()
  Description: Generates a new set of public-private key pairs for account creation.
  Parameters: None.

- EncryptAccountData(accountData, password)
  Description: Encrypts the account data using the provided password for secure storage.
  Parameters:
    - accountData (string): The account data to be encrypted.
    - password (string): The password to encrypt the account data.

- DecryptAccountData(encryptedData, password)
  Description: Decrypts the encrypted account data using the provided password.
  Parameters:
    - encryptedData (string): The encrypted account data to be decrypted.
    - password (string): The password to decrypt the account data.

- StoreAccountData(encryptedData)
  Description: Stores the encrypted account data securely.
  Parameters:
    - encryptedData (string): The encrypted account data to be stored.

- RetrieveAccountData()
  Description: Retrieves and decrypts the stored account data for use.
  Parameters: None.

**Account Class:**
Description: The Account class represents a Concordium account and stores relevant account information, such as public and private keys.

Methods:
- SignTransaction(transaction)
  Description: Signs the provided transaction using the account's private key.
  Parameters:
    - transaction (Transaction): The transaction object to be signed.

- GetAddress()
  Description: Retrieves the public address associated with the account.
  Parameters: None.

- GetPublicKey()
  Description: Retrieves the public key associated with the account.
  Parameters: None.

- GetPrivateKey()
  Description: Retrieves the private key associated with the account.
  Parameters: None.

**TransactionManager Class:**
Description: The TransactionManager class handles the construction, signing, and submission of transactions within the Concordium Unity SDK.

Methods:
- CreateTransferTransaction(senderAddress, recipientAddress, amount)
  Description:

 Constructs a transfer transaction with the specified sender, recipient, and amount.
  Parameters:
    - senderAddress (string): The sender's address.
    - recipientAddress (string): The recipient's address.
    - amount (decimal): The amount to be transferred.

- SignTransaction(account, transaction)
  Description: Signs the provided transaction using the specified account's private key.
  Parameters:
    - account (Account): The account object used for signing the transaction.
    - transaction (Transaction): The transaction object to be signed.

- SubmitTransaction(transaction)
  Description: Submits the signed transaction to the Concordium blockchain network for processing.
  Parameters:
    - transaction (Transaction): The signed transaction object to be submitted.

**ContractManager Class:**
Description: The ContractManager class handles smart contract interactions in the Concordium Unity SDK.

Methods:
- DeployContract(bytecode, constructorArgs)
  Description: Deploys a smart contract by constructing and submitting the necessary transaction to deploy the contract on the Concordium blockchain.
  Parameters:
    - bytecode (string): The bytecode of the smart contract.
    - constructorArgs (object[]): The arguments to be passed to the smart contract's constructor, if any.

- InvokeContractFunction(contractAddress, functionName, args)
  Description: Invokes a function of a deployed smart contract by constructing and submitting the necessary transaction to call the function on the Concordium blockchain.
  Parameters:
    - contractAddress (string): The address of the deployed smart contract.
    - functionName (string): The name of the function to be invoked.
    - args (object[]): The arguments to be passed to the function.

**Future Improvements:**

1. Enhanced Transaction Management:
   - Implement methods to retrieve transaction history for a specific account, allowing developers to fetch and display transaction details.
   - Add support for multi-signature transactions, enabling transactions that require multiple signatures from different parties.

2. Gas Estimation:
   - Integrate a gas estimation mechanism that calculates the estimated gas cost for a transaction before it is submitted to the blockchain. This can help users make informed decisions about transaction fees.

3. Event Filtering:
   - Extend the EventManager class to support event filtering capabilities, allowing developers to specify criteria for the events they want to receive notifications for. This can optimize event handling and reduce unnecessary callbacks.

4. Token Management:
   - Introduce methods to handle token management, such as retrieving token balances, transferring tokens, and subscribing to token-related events.

5. Wallet Recovery Options:
   - Expand the wallet recovery options to include recovery from hardware wallets or other external wallet providers.

6. Batch Operations:
   - Implement batch operation methods to allow developers to bundle multiple transactions or operations into a single batch for efficient processing on the blockchain.

7. Gas Price Configuration:
   - Enable developers to configure the gas price for transactions, providing flexibility and control over transaction fees.

8. Integration with Unity UI (Demo Project):
   - Provide additional support and examples for integrating the Concordium Unity SDK with Unity's UI system, enabling seamless integration of blockchain functionalities into the game's user interface.

**Roadmap:**

Todo
