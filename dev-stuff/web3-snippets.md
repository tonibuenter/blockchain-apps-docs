# Web3 Snippets


## Listening to Events

```
contract.events.allEvents()
    .on('data', (event) => {
        console.log('Event:', event);
        // Process the event data as needed
    })
    .on('error', (error) => {
        console.error('Error:', error);
        // Handle errors gracefully
    });

```
