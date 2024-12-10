# Blockchain Chat System Whitepaper

## 1. Overview

The goal of this system is to provide a decentralized chat platform powered by blockchain technology, enabling peer-to-peer encrypted communication without the need for identity verification, while also featuring wallet functionality.  
Messages exchanged between users can only be decrypted by the owner of the message, and all messages feature a "self-destruct after reading" function to ensure the security and privacy of communications. The system also integrates a token economy mechanism, using the iChat token to incentivize interactions between users and service providers.

## 2. System Architecture

### 2.1 User Role
- **Permissions and Security:** Users gain access to the system through a mnemonic phrase. If the mnemonic phrase is lost, the user will not be able to recover access, so it must be securely stored.
- **Message Encryption:** All messages are end-to-end encrypted during transmission, with only the sender and receiver able to decrypt the message content.
- **Message Storage:** The system stores unread messages for a maximum of 6 hours. After this time, messages are automatically discarded. Read messages are discarded immediately to ensure "self-destruct after reading" privacy protection.
- **Offline Handling:** If the user is offline while sending a message, the message is discarded immediately without waiting for receipt.

### 2.2 Service Role
The service role represents nodes in the system responsible for message transmission and validation services. Each service role holds a certain number of iChat tokens and provides services for other users.

- **iChat Token Requirements:** To become a service role, users must hold at least one million iChat tokens to ensure the stability of the service role and the implementation of the incentive mechanism.
- **Service Registration and Discovery:** Service roles need to register with each other to validate node legality and ensure that each service node can obtain an up-to-date list of online service roles. This mechanism ensures that service roles can connect to other valid service nodes.
- **Message Transmission and Query:** Service roles provide an interface for users to check if they have new messages and to provide a list of currently online service roles, enabling users to select the best service node for connection.
- **User Role and Service Node Connection:** Users need to connect to at least five service nodes when sending messages to ensure the message reaches its destination quickly and securely.  
  Each user needs to connect to at least five service nodes simultaneously to ensure reliable monitoring of unread messages in the system.

### 2.3 Reward and Punishment Mechanism
The existence and contributions of service roles are supported through token incentives, ensuring the long-term operation and activity of the system.

- **Reward Mechanism:**  
  Users who become service roles can earn iChat tokens by providing services. For each hour of service provided, the system rewards the corresponding amount of tokens based on the service duration.  
  Rewards are automatically distributed after users complete one hour of service. Services provided for less than one hour will not be rewarded.
- **Punishment Mechanism:**  
  Service roles that do not meet quality standards will be flagged by the system and have their iChat token rewards reduced. This includes behaviors such as high connection latency, message loss, system crashes, and frequent disconnections.

- **Token Circulation and Incentives:**  
  iChat tokens circulate within the system through interactions between service roles and user roles. When sending messages, users can also pay a certain amount of tokens based on the number of service nodes they are connected to, as a reward for the service roles.

## 3. Technical Implementation and Security

### 3.1 Blockchain Technology
This system will be built on blockchain technology, creating a decentralized chat and service network. All transaction records, token transfers, and user messages will be encrypted and stored on the blockchain, ensuring data immutability and transparency.

### 3.2 Encrypted Communication
- **End-to-End Encryption:**  
  All messages between users are encrypted using symmetric encryption and public-private key encryption techniques, ensuring that only the communicating parties can decrypt and read the message content.
- **Private Key Management:**  
  Users' private keys and wallet data will be stored locally with encryption to prevent leaks. Users must use a mnemonic phrase to recover and authorize their accounts.

### 3.3 Incentive and Economic Model
iChat tokens will form the incentive mechanism within the system:
- **User Rewards:**  
  User roles earn token rewards by sending messages and participating in network activities (e.g., verifying transactions, propagating messages).
- **Service Rewards:**  
  Service roles earn token rewards based on service duration and quality.
- **Token Circulation:**  
  iChat tokens not only serve as an incentive within the system but can also be traded on exchanges, providing a diversified economic model.

## 4. Future Development

- **Expanding Features:**  
  As user demand grows, the system can integrate additional features such as group chat, voice chat, video chat, etc.
- **Cross-Chain Integration:**  
  In the future, the system may consider integrating with other blockchain platforms to provide more token support and cross-chain functionality.
- **Enhanced Privacy Protection:**  
  By introducing more advanced encryption technologies and protocols, the system will further enhance user privacy and security.

### 4.1 Future Development and Revenue Model
1. As the user base grows, the value of the token will gradually rise, which is one of the profit models for early investors.
2. With a sufficient user base, commercial advertisements can be introduced in the client software. The revenue generated will be used to buy back and burn tokens.
3. Additional profit models are under development.

### 5. Timeline
- **Demo Version Launch:** January 10, 2025
- **Official Version Launch:** February 10, 2025
