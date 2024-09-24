# Shared Secret Store

The SharedSecretStore smart contract has the following features:

- The deployer (owner) creates a contract instance with a string. This string is an encrypted secret (eg.: nacl.keypair.secretkey). The secret is inserted into a map such as mapping(address->string) secrets
- The deployer can add and remove encrypted secrets entries for any user (address). 
- A user needs to have his public key saved in the PublicKeyStore contract.
- Except the deployers entry can  not be removed.
- Any user (address) can get his/hers encrypted secret string.
- Usually the encrypted secret for an address is a common secret key encrypted with the public key of the user (
  address). In this way a secret can safely be shared by multiple uses.
