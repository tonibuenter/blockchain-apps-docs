# DApp Universum

A business application will cover many contracts.

A set of business application also need to be managed so that there is a reliable source of truth to see what belongs to
an application, what is shared, what is in test, what is de-commissioned.

**Main goal of the DApp Universum** is the possibility to navigate within a DApp from one contract to another with names
instead with addresses.

For that purpose the following opinionated ordering concept is suggested.

## Universal Naming Service (UNS) (contract)

On a blockchain a single Universal Naming Service is used for a global entry for a company, a person, a group etd.
Comparable to a domain name a company 'MY-COMPANY' registers its primary contract. In our case a Contract Registry.

The Universal Naming Service (UNS) has the following characteristics:

- One deployment per blochchain is enough
- Everybody can register a unique name
- Rule: First come first serve
- For security: Only capital letters, dashes and dots (like domain names).
- As a spam protection a small fee is required for registration (less than 10$).
- No governance: not even contract owner can delete, change or reassign names.
- Contract owner can only withdraw the collected fees.

## Contract Registry (contract)

As mentioned the Contract Registry is often registered with the UNS name.
A Contract Registry has the following characteristics:

- Owner: company responsible
- Individual mapping of address to names such as 0x234 to ADDRESS_BOOK


