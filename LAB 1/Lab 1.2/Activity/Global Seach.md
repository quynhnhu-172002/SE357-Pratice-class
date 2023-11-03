@startuml Activity_GlobalSearch

title Activity Global Search

start
:User enters search keyword;
if (Search successful?) then (Yes)
  :Display search results;
else (No)
  :Display "No results found" message;
endif
stop
@enduml
