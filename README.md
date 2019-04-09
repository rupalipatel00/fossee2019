# fossee2019
Provenance tracking - Following the chain of custody and authenticity of an asset:-

Here I have considered asset as property and have designed the architecture and sol file on that basis only.

Architecture involves:-


1. User - User who owns the asset and wants to either sell it or purchase another asset.
2. Admin - Admin who will validate each transaction and this admin will be randomly chosen. The functionality of admin is to register new assets and approve assets title transfer request.
3. SuperAdmin - Who will form the admins and change user domains


Description of few important transactions - 

* addUser() -
1. Name
2. Aadhar number
3. User ID/ Ethereum ID
    On taking the above parameters it adds the user under the admins.

 * changeUserDomain()-
1. User ID / Ethereum ID
2. User Type
    On taking the above parameters, Superadmin changes the user domain to admin domain.

* addRecord() - 
1. Seller’s Address
2. Buyer’s Address
3. Property ID
4. Memory IPFS Hash
   On taking the above parameters, it adds or registers user asset/property transaction.

* removePropertyRequest() - 
1. User ID/ Etheruem ID
2. Request ID
   On taking the above parameters, user can remove the property request.

* addproperty() - 
1. UserID
2. Request ID
	This function adds the new property on the list of properties.

* notify() -
1. Request ID
	This function is to notify the admin for requests related to property registering and transaction.

* approve() - 
1. Request ID
	This function approves the transaction request of the users.


Other functions have been described in solidity file itself.
