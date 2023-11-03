@startuml

actor User
participant "System" as Sys
User -> Sys: Enter username and password
User -> Sys: Click 'Login'
activate Sys
Sys -> Sys: Validate credentials
alt Invalid Credentials
  Sys -> Sys: Display error message
  User --> Sys: Retry
else Valid Credentials
  Sys -> Sys: Redirect to dashboard
  User --> Sys: Successfully logged in
end

@enduml
