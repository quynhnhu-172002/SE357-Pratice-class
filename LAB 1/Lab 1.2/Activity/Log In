@startuml Activity_DangNhap
!define START circle
!define END circle
!define ACTIVITY_START start
!define ACTIVITY_END end

title Activity Đăng nhập

start

:Người dùng nhập thông tin đăng nhập;
:Hệ thống kiểm tra thông tin đăng nhập;
if (Thông tin đúng?) then (Đúng)
  :Người dùng được đăng nhập;
  -[Hệ thống]-|Hệ thống xác thực tài khoản|;
  :Mở trang chủ;
else (Sai)
  :Hiển thị thông báo lỗi;
  -[Hệ thống]-|Hệ thống xác thực tài khoản|;
  stop
endif

stop

@enduml
