<div style="border-bottom: solid gray 1px;text-align:  right"><h3 style="alignment-baseline: center">An <img src="../images/ooit-logo-300x100.png" alt="ooit logo" width="70" height="26"> Initiative</h3></div>

# Solution for Lost or Stolen Keys

## Mitigating Risks from Lost or Stolen Private Keys

Losing or having your private key stolen can be disastrous. If a malicious actor gains access to your private key, they
can control your associated address and its assets. Here are some ways to mitigate these risks.

## Central Authentication and Role Manager (CAARM)

A CAARM contract can help address key loss by:

- **Address Resolution**: Providing the original or a replacement address for a given user.
- **Role-Based Authorization**: Maintaining a list of roles a calling contract can use for authorization.
- **Trust Requirement**: The owner of the CAARM must be trustworthy.

### CAARM Use Cases

- **Address Change**: A user can change their address from A to B.
- **Role Transfer**: Transfer roles associated with address A to address B.
- **Address Blocking**: Block a compromised address.
- **Updating Applications**: Update address books and secure blockchain tables to reflect the new address.

### CAARM Usage in Client Contracts

Instead of directly using `msg.sender`, client contracts should use `carm.resolveAddress(msg.sender)` to get the
potentially
updated address.

## Bounty Concept for Lost Keys

The Bounty Concept offers an alternative to relying on a trusted CAARM owner:

+ **Registration**: A user claiming to be the owner of address A registers a new address B as the replacement, along
  with a bounty.
+ **Blocking**: Address A is blocked for a waiting period (e.g., a week or a month).
+ **Real Owner Recovery**: If the real owner detects the block, they can unblock A and claim the bounty.
+ **Key Loss Scenario**: If the user genuinely lost their key, they can use the new address B after the waiting period
  and claim the bounty.

## Key Points

- Losing a private key can have serious consequences.
- CAARM and the Bounty Concept offer ways to mitigate risks, but each has its own tradeoffs.
- CAARM relies on a trusted owner, while the Bounty Concept uses a financial incentive mechanism.
- Consider these options carefully to choose the best approach for your specific needs and risk tolerance.
