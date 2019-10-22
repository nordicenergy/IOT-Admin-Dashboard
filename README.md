# Nordic Energy´s - IOT Platform & Admin Dashboard 

### - A Blockchain-based Service for Smart Home System Using EOSIO Blockchain: System and Architecture.



#### Angular Admin Dashboard:

- Admin + backend (.NET, Node.js, Java etc.) = ready-made solution for data management. 




#
### Emergency Service For Smart Home Systems Using Eosio Blockchain DApps: System and Architecture

Due to emerging disruptive technologies, play a vital role for smart living domains, for examples, elderly and disabilities healthcare services, home safety, security, energy monitoring and automation control services. Our systems will send automatically an emergency call with home user information and location as a privacy data to public services like hospitals, police offices, or fire departments. Emergency service for a Smart Home System (SHS) based on EOSIO blockchain with smart contract for decentralized ledger technology handling access control among untrusted public services so called Home Service Providers (HSPs) and smart home IoT devices. 


Establishing safe and secure living environment goes beyond protecting residents from a variety of threats like accidental injuries, crimes and life-threatening situations. Therefore, 24/7 monitoring and controlling safety and security services for residents such as elderly people, disabilities and independent living families increasingly demand for smart home Internet of Things (IoT), which require to send automatically an emergency call to public services like hospitals, police stations, fire departments, or household maintenances according to any abnormal situations. User information and home location transferred to those public services need to be protected from various of cyber-attacks according to GDPR and CBPR. 


Due to various types of cyber-attacks such as Botnets, Distributed Denial of Service (DDoS), data and identity theft, home users are wary of using Smart Home System (SHS). Nordic Energy´s IoT platform propose an EOSIO (EOS) blockchain based Home Service Solution (HSS) with smart contract for decentralized handling transaction control among HSPs and SHSs. Our proposed Smart Home System is composed of Sensor Management System (SMS) and eosio.cd and provides programmable smart contracts to trigger transactions automatically with specified conditions. It also provides both private and public blockchain. Private blockchain allows only the specified members of the P2P network to deal with the distributed records. Moreover, different roles of members are allowed only read permission in distributed records. We choose EOSIO blockchain for our proposed work due to homeowner’s privacy information and the immutability of data transaction, auditability, integrity and authorization. 



### Smart Contract 

Nordic Energy to develop smart contract on private blockchain. According to our smart contracts are written in Eosio scripting language and compiled at Remix to get JSON Application Binary Interface (ABI). This ABI with the EOS contract address are used to call the smart contract function as a transaction within the EOSIO-based private blockchain.



### Data Encryption 

Is to protect user data or sensitive information from eavesdropper during data-in-transit. In our proposed work, we use RSA asymmetric encryption algorithm and the key length is 1024-bit. RSA can be used for both “data encryption” and “digital signature”. 



### InterPlanetary File System (IPFS)

IPFS is an open-source, content-addressable, and peer- to-peer (P2P) method of storing and sharing hypermedia in a distributed system. IPFS addresses file location with the content itself. This is done by using a cryptographic hash on the file. At our proposed work, we combine IPFS and Eosio in distributed miner systems. The IPFS will be used to send an emergent incident from each home sensor management system to a regional miner technology. 



### What is the InterPlanetary File System (IPFS)? 

The InterPlanetary File System (IPFS) is a protocol and peer-to-peer network for storing and sharing data in a distributed file system. IPFS uses content-addressing to uniquely identify each file in a global namespace connecting all computing devices. IPFS allows users to not only receive but host content, in a similar manner to BitTorrent. As opposed to a centrally located server, IPFS is built around a decentralized system of user-operators who hold a portion of the overall data, creating a resilient system of file storage and sharing. Any user in the network can serve a file by its content address, and other peers in the network can find and request that content from any node who has it using a distributed hash table (DHT).



### Authentication

Authentication is a process to verify the identity of users or IoT devices to be able to access computing system, blockchain network, resources or applications. It is used to make sure that only the trusted members or IoT devices can make a transaction with smart home systems. 



### Sensor Management System Installation and Configuration 

Start to deploy Raspberry Pi (RPi) as the sensor management system, IoT gateway and blockchain client, and apply IPFS to distribute an emergency call. We install python IPFS and geth on RaspberryPi.



#### To start the our private blockchain, a “genesis” file with the specified parameters. is initialized with the command:

“geth   datadir ~/eosio/rpi/init genesis.json”. 



#### The service of IPFS is started with “ipfs daemon” and configured its default port number of HTTP RPC API from the python script file as follows:

“ipfsAPI=ipfsApi.Client(‘a.b.c.d’,5001, {protocol: ‘http’})”, where a.b.c.d is the current IP address of Sensor Management System (SMS).



#### When the SMS sends an emergency call to EM, the operations will be as follows Sensor Management System encrypts the emergency call with the RSA public key of EM node like:

“encrypted_emergencyCall=rsa_EM public Key.encrypt ('Emergency Call.json',32)” with the attachment of digital signature as: 
“signature = hexlify (rsa.pkcs1.sign (HoInfo, privkey, 'SHA-256'))”, where pkcs1 performs RSA algorithm to generate Public Key Cryptographic Signature. 



#### Sensor Management System uploads the encrypted emergency call as:

“ipfs Loaded File=api.add('encrypted_en crypted_emergency Call.json')”, to the IPFS peers. 



#### EM receives the encrypted emergency call from the hash distributed by Sensor Management System and decrypts with its own RSA private key to retrieve the type of emergency:


- Smart Contract Creation. 
- Emergency Type Identification. 
- Emergency call for home security squad´s. 
- Home security squad response for the emergency call. 
- QR code generation for the home security privacy staff to get access control at house. 
- Service fee transfer from home owner’s wallet to home security squad´s

