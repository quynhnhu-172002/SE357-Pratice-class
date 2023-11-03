@startuml
actor User
User -> System: Start Export

User -> System: Define Export Criteria
System --> User: Provide Export Options

User -> System: Set Export Configuration
System --> User: Confirm Export Settings

User -> System: Initiate Export
System -> Database: Query Database for Student Information
Database --> System: Retrieve Student Data
System -> System: Format Data for Excel
System -> System: Generate Excel File
System --> User: Provide Excel Download Link

User -> System: Download Excel File

User -> System: End Export

@enduml
