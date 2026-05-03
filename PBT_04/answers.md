CÂU A1:
Position	Vẫn chiếm chỗ trong flow?	        Tham chiếu vị trí	                  Cuộn theo trang?	        Use case

static		Có                          top, right, bottom, left không hoạt động       Có                 Mặc định mọi phần tử

relative	Có                          Tham chiếu vị trí của chính nó                 Có             Dịch chuyển nhẹ các element

absolute	Không                       Phần tử cha có relative                        Có             Badge, dropdown, tooltip, overlay

fixed		Không                       Tham chiếu đến viewport                        Không      Chat button, cookie banner, header cố định

sticky		Có                          Tham chiếu đến viewport (khi dính)             Có         Sticky header,sticky table header, sidebar

Trả lời câu hỏi thêm: 
    1.Khi nào absolute tham chiếu body?
    Khi không có phần tử nào là position: relative , absolute , fixed hoặc sticky chứa nó
    2. Khi nào tham chiếu parent?
    Khi parent trực tiếp hoặc gián tiếp có position: relative, absolute, fixed hoặc sticky (thường dùng relative cho parent).
    3.Giải thích khái niệm "nearest positioned ancestor"
    Là phần tử bao ngoài gần nhất (tính từ phần tử đang xét) có thuộc tính position.

CÂU A2:
    Trường hợp 1:
    4 items tạo thành 1 hàng ngang
    -text art:
    [ Item 1 ] [ Item 2 ] [ Item 3 ] [ Item 4 ]

    Trường hợp 2:
    Mỗi hàng 2 items (45% + 2.5% left + 2.5% right = 50% × 2 = 100%)
    có 6 items -> có 3 hàng và 2 cột
    flex-wrap: wrap giúp xuống dòng nếu không đủ chỗ
    -text art:
    [ Item 1 ] [ Item 2 ]
    [ Item 3 ] [ Item 4 ]
    [ Item 5 ] [ Item 6 ]

    Trường hợp 3:
    3 items tạo thành 1 hàng ngang, khoảng cách giữa các item bằng nhau
    -text art:
    [ Item 1 ]            [ Item 2 ]            [ Item 3 ]

    Trường hợp 4:
    3 items tạo thành 1 hàng có 3 cột
    +Cột 1: cố định 200px
    +Cột 2: co giãn chiếm phần còn lại (1fr)
    +Cột 3: cố định 200px
    +Giữa các cột có gap (tạo khoảng cách) 20px
    - text art:
    [ Item 1 ] <---gap 20px--> [      Item 2       ] <---gap 20px---> [ Item 3 ]
    200px                               1fr                             200px

    Trường hợp 5:
    Mỗi hàng 3 items (vì repeat(3, 1fr))
    + Hàng 1: items 1, 2, 3
    + Hàng 2: items 4, 5, 6
    + Hàng 3: chỉ có item 7 ở cột đầu tiên, cột 2 và 3 để trống
    + gap: 10px giữa các item (cả hàng và cột)
    - text art:
    [ Item 1 ] [ Item 2 ] [ Item 3 ]
    [ Item 4 ] [ Item 5 ] [ Item 6 ]
    [ Item 7 ] [  trống ] [  trống ]



