@startuml Activity_Login

!define START circle
!define END circle
!define ACTIVITY_START start
!define ACTIVITY_END end

title Activity Log In 

start

:User enters login information;
:System verifies login information;
if (Information is correct?) then (Correct)
  :User is logged in;
  -[System]-|System authenticates the account|;
  :Open homepage;
else (Incorrect)
  :Display error message;
  -[System]-|System authenticates the account|;
  stop
endif

stop

@enduml
