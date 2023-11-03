@startuml
title Activity Tìm kiếm toàn cục

start
:Người dùng nhập từ khóa tìm kiếm;
if (Tìm kiếm thành công?) then (Có)
  :Hiển thị kết quả tìm kiếm;
else (Không)
  :Hiển thị thông báo "Không tìm thấy kết quả";
endif
stop
@enduml
