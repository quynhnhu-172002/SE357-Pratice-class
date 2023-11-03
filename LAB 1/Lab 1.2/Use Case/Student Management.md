@startuml ManageStudents

left to right direction

actor Admin as A
actor "Student" as S
rectangle "STUDENT MANAGEMENT" {
A --|> (Import students from Excel file)
A --|> (Create new student)
A --|> (Search for a student using search bar)
A --|> (Search for a student using default filter)
A --|> (Create new search filter)
A --|> (View list of students)
A --|> (View detailed student information)
A --|> (Delete one or more student records)
A --|> (Update student information)
A --|> (Export information of one or more students to Excel)
A --|> (Transfer fees to another student)
A --|> (Refund fees to a student)

S --|> (View detailed student information)
S --|> (Transfer fees to another student)
S --|> (Refund fees to a student)
}
@enduml
