@startuml
actor User
actor System
actor CallCenter

User -> System: Initiate SMS
User -> System: Compose Message
System --> User: Provide Recipient Options
User -> System: Select Recipient (Student/Parent)
System --> User: Enter Message Content
User -> System: Confirm Message

System -> CallCenter: Forward SMS Request
CallCenter -> CallCenter: Queue SMS for Sending
CallCenter -> CallCenter: Send SMS

CallCenter --> System: SMS Sent Confirmation
System --> User: SMS Sent Confirmation

User -> System: End SMS

@enduml
