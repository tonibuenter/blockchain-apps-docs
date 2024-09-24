# Solution for Lost or Stolen Keys

A lost or stolen key may inflict a lot of damage.

In general if the private key of an address A gets in the hand of a malicious actor there is not much to do to save assets or prevent
transactions to execute in the name of A.

Here some mitigation concepts that can be applied.

## Central Authentication And Role Manager

Use a central role manager  (CAARM) contract for

- resolving address, returning the original or a replacement address
- use a list of roles the calling contract can use for authorization
- Precondition: owner of the CAARM has to be trustworthy

### Example Use Cases for CAARM

- User wants to change address A to B
- Transfer roles from A to B
- Block A
- Address Book add B, remove A
- SecureBlockchainTable add B, remove A
- CentralRoleContract: transfer A to B

### Usage in a client contract

Instead of using
`msg.sender`
use
`carm.resolveAddress(msg.sender)`

## Bounty Concept for Lost Key

Instead of relying on a CARM trustworthy owner the Bounty Concept uses the following:

- Actor F pretending being the owner address A registers an address B as the replacement for address A
- In addition, the registration requires an essential amount of crypto money as a bounty
- After the registration the address A is blocked for a waiting period like a week or a month
- In case now the real owner R of A detects his address is blocked he can (because he hase the private key of A) unblock
  the address A and cash in the bounty
- In case of F is really the owner and she has lost the private key. F can use address B after the waiting period and
  cash in the bounty.
