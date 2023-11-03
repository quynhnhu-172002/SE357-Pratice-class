@startuml
actor User
User -> System: Start Search with Filter

User -> System: Select Filter Criteria
System --> User: Display Available Filter Options

User -> System: Set Filter Values
System --> User: Show Selected Filter Values

User -> System: Initiate Search
System -> Database: Query Database
Database --> System: Retrieve Search Results
System --> User: Display Search Results

User -> System: Create Filter
System -> User: Provide Filter Creation Form
User -> System: Define Filter Criteria
System --> User: Confirm Filter Creation
System -> Database: Save Filter

User -> System: Apply Saved Filter
System -> Database: Retrieve Saved Filter
System --> User: Display Selected Filter
System -> Database: Query Database with Filter
Database --> System: Retrieve Filtered Results
System --> User: Display Filtered Results

User -> System: End Search

@enduml