@startuml
class "Student" as Student {
  - studentId: int
  - name: string
  - email: string
  - phone: string
  - address: string
}
class "Call" as Call {
  callId: int
  caller: string
  receiver: string
  startTime: datetime
  duration: int 
}
class "Email" as Email {
  emailId: int
  sender: string
  receiver: string
  subject: string
  content: string 
}
class "SMS" as SMS {
  smsId: int
  sender: string
  receiver: string
  message: string 
}
class "Task" as Task {
  - taskId: int
  - title: string
  - description: string
  - assignedTo: string
  - dueDate: datetime
}
class "Teacher" as Teacher {
  - teacherId: int
  - name: string
  - email: string
  - phone: string
}
class "Lesson" as Lesson {
  - lessonId: int
  - title: string
  - content: string
  - teacher: string
}
class "Class" as Class {
  - classId: int
  - courseId: int
  - className: string
  - teacher: string
  - students: List<Student>
}
class "CourseFee" as CourseFee {
  - feeId: int
  - courseId: int
  - amount: float
  - dueDate: datetime
}
class "Gradebook" as Gradebook {
  - gradebookId: int
  - student: string
  - course: string
  - grade: float
}
class "Attendance" as Attendance {
  - attendanceId: int
  - class: string
  - student: string
  - date: datetime
  - status: string
}
class "Payment" as Payment {
  - paymentId: int
  - student: string
  - amount: float
  - date: datetime
}
class "Invoice" as Invoice {
  - invoiceId: int
  - student: string
  - amount: float
  - dueDate: datetime
}
class "Receipt" as Receipt {
  - receiptId: int
  - student: string
  - amount: float
  - date: datetime
}
class "User" as User {
  - userId: int
  - username: string
  - password: string
  - role: string
}
class "Kind of Course" as KindofCourse {
  - courseId: int
  - coursecategory: string
  - coursename: string
  - lessonplan: <List>Lesson
}

Student "1" -- "0..*" Class: has
Teacher "1" -- "0..*" Class : manage
Payment "1" -- "0..*" CourseFee : has
Class "1" -- "0..*" Gradebook : has
Class "1" -- "0..*" Attendance : has
Student "1" -- "0..*" Payment : has
Student "1" -- "0..*" Call : has
Student "1" -- "0..*" SMS : has
Student "1" -- "0..*" Email : has
Payment "1" -- "1" Invoice : has
Payment "1" -- "1" Receipt : has
Class "1" -- "1" KindofCourse : has
KindofCourse "1" -- "0..*" Lesson : has
Student "1" -- "0..*" Attendance : has
@enduml
