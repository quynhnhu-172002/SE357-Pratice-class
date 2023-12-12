@startuml
class "Student" as Student {
  - studentId: int
  - name: string
  - email: string
  - phone: string
  - address: string
  + enrollInClass(class: Class): void
  + makePayment(amount: float, date: datetime): void
  + makeCall(receiver: string, startTime: datetime, duration: int): void
  + sendEmail(receiver: string, subject: string, content: string): void
  + sendSMS(receiver: string, message: string): void
}

class "Call" as Call {
  - callId: int
  - caller: string
  - receiver: string
  - startTime: datetime
  - duration: int
  + answerCall(): void
  + endCall(): void
}

class "Email" as Email {
  - emailId: int
  - sender: string
  - receiver: string
  - subject: string
  - content: string
  + reply(): void
  + forward(to: string): void
}

class "SMS" as SMS {
  - smsId: int
  - sender: string
  - receiver: string
  - message: string
  + reply(): void
}

class "Task" as Task {
  - taskId: int
  - title: string
  - description: string
  - assignedTo: string
  - dueDate: datetime
  + completeTask(): void
}

class "Teacher" as Teacher {
  - teacherId: int
  - name: string
  - email: string
  - phone: string
  + assignTask(task: Task): void
  + conductClass(): void
}

class "Lesson" as Lesson {
  - lessonId: int
  - title: string
  - content: string
  - teacher: string
  + teach(): void
}

class "Class" as Class {
  - classId: int
  - courseId: int
  - className: string
  - teacher: string
  - students: List<Student>
  + addStudent(student: Student): void
  + conductClass(): void
}

class "CourseFee" as CourseFee {
  - feeId: int
  - courseId: int
  - amount: float
  - dueDate: datetime
  + payFee(): void
}

class "Gradebook" as Gradebook {
  - gradebookId: int
  - student: string
  - course: string
  - grade: float
  + viewGrade(): void
}

class "Attendance" as Attendance {
  - attendanceId: int
  - class: string
  - student: string
  - date: datetime
  - status: string
  + markAttendance(status: string): void
  + viewAttendance(): void
}

class "Payment" as Payment {
  - paymentId: int
  - student: string
  - amount: float
  - date: datetime
  + viewPaymentDetails(): void
}

class "Invoice" as Invoice {
  - invoiceId: int
  - student: string
  - amount: float
  - dueDate: datetime
  + viewInvoice(): void
  + printInvoice(): void
}

class "Receipt" as Receipt {
  - receiptId: int
  - student: string
  - amount: float
  - date: datetime
  + viewReceipt(): void
  + printReceipt(): void
}

class "User" as User {
  - userId: int
  - username: string
  - password: string
  - role: string
  + login(): void
  + logout(): void
}

class "Kind of Course" as KindofCourse {
  - courseId: int
  - coursecategory: string
  - coursename: string
  - lessonplan: <List>Lesson
  + viewLessonPlan(): void
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
User "1" -- "0..*" Task: has
@enduml
