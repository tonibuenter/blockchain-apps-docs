
# Databases on EVM Blockchains

## Pure

The pure and simple approach when it comes to databases on EVM Blockchains is just to use structs, mapping and arrays.

There are a couple of patterns that helps to keep a table like data structure clean:
```
struct MyTable {
   //columns...
}
```
## Tableland

Tableland uses SQLLight as 'classical' backend layer. 

In a nutshell:

- Reading from the backend SQLLight
- Changing statements such as insert/update/delete are added to the Tableland contract
- A successful add transaction creates an SQLEvent
- The SQLEvents are applied to the database by the SQLLight backend

https://github.com/tablelandnetwork/evm-tableland
