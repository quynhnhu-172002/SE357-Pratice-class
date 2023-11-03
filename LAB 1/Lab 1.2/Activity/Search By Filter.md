@startuml
title Activity Tìm kiếm bằng filter

start

:Người dùng chọn bộ lọc;
if (Chọn bộ lọc) then (Có)
  :Người dùng nhập thông tin tìm kiếm;
  if (Nhập thông tin tìm kiếm) then (Có)
    :Thực hiện tìm kiếm theo bộ lọc;
    :Hiển thị kết quả tìm kiếm;
  else (Không)
    :Hiển thị thông báo lỗi;
  endif
else (Không)
  :Hiển thị tất cả dữ liệu;
endif

stop

@enduml
