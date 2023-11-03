@startuml
left to right direction
!define ICONURL https://www.plantuml.com/g?icon=

actor "User" as User
rectangle "KIND OF COURSE" {
  usecase (Import List Course\nfrom Excel) as Import
  usecase (Search Course\nby Keyword) as Search
  usecase (Filter Courses\nby Default) as Filter
  usecase (Create New\nCourse) as Create
  usecase (View Course\nList) as ViewList
  usecase (View Course\nDetails) as ViewDetails
  usecase (Update Course\nInformation) as Update
  usecase (Delete Course) as Delete
  usecase (Duplicate Course) as Duplicate
  usecase (Export Course\nInformation) as Export
}

User --> Import 
User --> Search 
User --> Filter 
User --> Create 
User --> ViewList 
User --> ViewDetails 
User --> Update 
User --> Delete 
User --> Duplicate 
User --> Export 

@enduml
