@startuml

skinparam handwritten true

title Activity Diagram: Create Students

start

:Choose Function (Create Student/Upload Excel);
if (Create Student is chosen) then (yes)
  :Check Duplicate (Mobile/Name);
  if (Duplicate Found?) then (yes)
    :Display Duplicate Found Options;
    if (Choose to Merge) then (yes)
      :Merge Duplicate Students;
    else (no)
      :Edit Duplicate Student Information;
    endif
  else (no)
    :Create Student;
    :Enter Personal Information;
    :Select User (Responsible);
    :Save Student Information;
  endif
else (no)
  :Upload Excel File;
  if (Excel File Uploaded) then (yes)
    :Process Excel Data;
    :Map Properties;
    :Check duplicate;
    :Update student information;
  else (no)
  endif
endif

stop

@enduml
