@startuml

skinparam handwritten true

title Activity Diagram: Create Payment

start

:Select Student (Student);
:Select Payment Type (Payment Type);
:Select Course Category (Course Category);
:Enter Total Paid Amount (Paid Amount);
:Enter Payment Date (Payment Date);

:Select Payment Type (Payment Type);

if (Payment Type is equal to "Cashholder") then (yes)
  :Create Cashholder Payment (Cashholder);
  :Select Split Payment (if needed?);
  if (Split Payment is needed) then (yes)
    :Enter Number of Installments;
  else (no)
  endif
else (no)
  if (Payment Type is equal to "Deposit") then (yes)
    :Create Deposit Payment (Deposit);
  else (no)
    if (Payment Type is equal to "Placement Test") then (yes)
      :Create Placement Test Payment (Placement Test);
    else (no)
      if (Payment Type is equal to "Delay Fee") then (yes)
        :Create Delay Fee Payment (Delay Fee);
      else (no)
        if (Payment Type is equal to "Book/Gift") then (yes)
          :Create Book/Gift Payment (Book/Gift);
        endif
      endif
    endif
  endif
endif

:Save Payment Information;


stop

@enduml
