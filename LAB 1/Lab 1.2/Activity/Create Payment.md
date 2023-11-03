@startuml
!theme cerulean

skinparam handwritten true

title Activity Diagram: Quy trình Tạo Thanh Toán Học Phí

start

:Chọn Học Viên;

if (Học Viên có trên hệ thống chưa?) then (yes)
  :Tạo Học Viên Mới;
  :Nhập Thông Tin Học Viên;
  if (Thông tin hợp lệ?) then (yes)
    :Thêm Học Viên Mới;
  else (no)
    :Sửa Thông Tin;
  endif
else (no)
  :Chọn Học Viên Tồn Tại;
endif

:Tạo thanh toán mới ;

  :Nhập Thông Tin Loại Thanh Toán;
  if (Thông tin hợp lệ?) then (yes)
    :Thêm Loại Thanh Toán Mới;
  else (no)
    :Sửa Thông Tin;

endif

:Chọn Loại Khóa Học (Course Category);
:Nhập Tổng Tiền Đã Thanh Toán (Paid Amount);
:Chọn Ngày Thanh Toán (Payment Date);

if (Loại Thanh Toán là Deposit) then (yes)
  :Tạo Thanh Toán Deposit;
  :Lưu Thông Tin Thanh Toán;
else (no)
  if (Loại Thanh Toán là Placement Test) then (yes)
    :Tạo Thanh Toán Phí Thi Thử;
    :Lưu Thông Tin Thanh Toán;
  else (no)
    if (Loại Thanh Toán là Demo) then (yes)
      :Tạo Thanh Toán Phí Học Thử;
      :Lưu Thông Tin Thanh Toán;
    endif
  endif
endif

stop

@enduml
