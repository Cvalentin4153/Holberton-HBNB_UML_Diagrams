```mermaid
sequenceDiagram

participant User
participant API
participant BusinessLogic
participant Database

User->>API: API Call +createUser()
API->>BusinessLogic: +processRequest() validateRequest()
BusinessLogic->>Database: Save and Store Data
Database-->BusinessLogic: Confirm Data Storage
BusinessLogic-->API: Return User
API-->User: Return Success/Failure
```