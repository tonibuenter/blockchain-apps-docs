


# Secure Blockchain Table (SBT)

The Secure Blockchain Table (SBT) is a blockchain-based data structure for storing lists of rows. Each row typically contains:

- **Encrypted Data**: The actual information you want to store, kept confidential.
- **Index**: A unique identifier for the row.
- **User Address**: The blockchain address associated with the row.
- **Version**: Tracks changes to the row over time. 

Think of the index and version as two dimensions of the table. The content can be any structured data, like a row in a traditional spreadsheet.

Beyond storing rows, SBT contracts also support:

- **Metadata**: Information about the structure and meaning of the data.
- **Initial Data**: Pre-populated rows to start with.
- **User Management**: Control who can access and modify the data.
- **Secret Store**: A secure place for authorized users to store sensitive information.

## Real-World Example: Salary Manager

### Owner Setup:

- Creates a new SBT contract.
- Adds authorized users.
- Uploads an Excel sheet as initial data.

### User Actions:

- Loads the initial data.
- Views and edits specific rows.
- Saves changes, creating new versions of the rows.
- Reviews data and version history.

### User Management:

- The owner can add or remove users as needed.

### Owner Finalizes:

- Sets the contract to read-only, preventing further changes.


### Key Points:

- SBTs provide a secure and tamper-proof way to store structured data on the blockchain.
- They support version control and user access management.
- SBTs can be used for various applications, like managing salaries, tracking inventory, or storing sensitive documents.
