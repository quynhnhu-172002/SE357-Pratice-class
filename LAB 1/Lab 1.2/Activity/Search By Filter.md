@startuml Activity_FilteredSearch

title Filtered Search Activity

start

:User selects a filter;
if (Filter selected) then (Yes)
  :User enters search information;
  if (Enter search information) then (Yes)
    :Perform search using the selected filter;
    :Display search results;
  else (No)
    :Display error message;
  endif
else (No)
  :Display all data;
endif

stop

@enduml
