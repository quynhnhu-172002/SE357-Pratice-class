@startuml CallManagement

left to right direction

actor Admin as A
actor User as U
rectangle "CALL MANAGEMENT" {
A --|> (Import Call/Appointment data from Excel file)
A --|> (Create Call)
A --|> (Log Call Information)
A --|> (Search Calls using Search Bar)
A --|> (Search Calls using Default Filter)
A --|> (Create Search Filter)
A --|> (Delete one or multiple Calls)
A --|> (Update Call Information)
A --|> (View Call Information)
A --|> (View List of Calls)

U --|> (Log Call Information)
U --|> (View Call Information)
U --|> (View List of Calls)
}
@enduml
