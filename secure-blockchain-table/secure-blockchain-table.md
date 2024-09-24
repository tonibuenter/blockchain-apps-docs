# Secure Blockchain Table (SBT)

The Secure Blockchain Table is a storage of a list of rows.
A row consists of a content  (usually the encrypted data), index, a user address and a version.
Index and version can be looked at as two dimensions. The content could be a list of values like a table row.

Next to the rows the SBT contract allows to save 
- Meta data (structural data for the interpretation of the data)
- Initial data (e.g. a set of starting rows)
- User management 
- A secret store for entitled users

If this is a bit abstract, here a real world exmple:

## Salary Manager

### Owner starts Salary Manager cycle

- Owner create new SBT contract
- Owner adds users (entitled users)
- Owner upload excel as initial data


### Entitled User

- User loads initial data
- User loads data rows
- User edits data row
- User saves data row
- User reloads data
- Users check versions

### Owner ends Salary Manager cycle

- Owner set contract to readonly


### Owner adds/removes users

- Owner adds user
- Owner removes user
