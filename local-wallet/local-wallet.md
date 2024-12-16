# Local Wallet

We chose the `etherjs` Local Wallet over MetaMask and similar plugin wallets due to the lack of functionality and convenience. The Local Wallet data is encrypted and saved to the browser's local storage.

### Comparison to MetaMask Wallet:

| Topic             | MetaMask Plugin Wallet                                       | Rating       | Local Wallet (etherjs)                                | Rating        |
|-------------------|--------------------------------------------------------------|--------------|-------------------------------------------------------|---------------|
| Security          | Encrypted with wallet password                               | ⭐️⭐️⚪&nbsp;🔓🔓⚪  | Same                                                  | ⭐️⭐️⚪&nbsp;🔓🔓⚪   |
| Passphrase        | Provides passphrase for wallet and internal accounts         | ⭐️⭐️⚪&nbsp;🔓🔓🔓 | All accounts are external                             | ⭐️⭐️⚪&nbsp;🔓🔓🔓  |
| Key Management    | User must keep wallet password and passphrases safe          | ⭐️⭐️⚪ 🔓🔓🔓 | User must keep wallet password and passphrases safe   | ⭐️⭐️⚪ 🔓🔓🔓  |
| Connecting Wallet | Can connect to any website                                   | ⭐️⭐️⭐️ 🔓🔓⚪ | Connection only used for the original website         | ⭐️⭐️⚪ 🔓🔓🔓  |
| Data encryption   | Does not provide data encryption with public/private key     | ⚪⚪⚪ 🔓⚪⚪     | Uses `eth-crypto` for data encryption                 | ⭐️⭐️⭐️ 🔓🔓🔓 |
| Confirmation      | Requires user confirmation for every transaction and signing | ⭐️⚪⚪ 🔓🔓🔓  | Full access to account, no user confirmation required | ⭐️⭐️⭐️ 🔓🔓⚪  |

Rating: Convenience: ⭐️, Security: 🔓

### Conclusion

The security of the Local Wallet is comparable to MetaMask. Users must trust both the wallet provider and the Web3 
application. The Local Wallet may seem less secure as it does not require user confirmation for transactions and signings. Keeping passphrases safe is 
crucial in both cases. Wallet data can be lost by re-installing the browser or clearing application data, but can be recovered with secret passphrases or private keys.
