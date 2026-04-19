CÂU A1:
    1.
        Khi ta mở chrome và gõ https://shopee.vn sau đó nhấn phím enter.
            1.Request xuất phát từ máy tính cá nhân -> đi qua router wifi  
            -> Qua nhà mạng -> chạy qua cáp quang 
            2. -> Đến data center của Shopee ở Việt Nam
            3. -> Server xử lý: "Tôi muốn truy cập trang chủ Shopee"
            4. -> Response chạy ngược lại: cáp quang -> nhà mạng -> router -> máy tính cá nhân
            5. -> Chrome nhận file HTML,CSS,JS -> render ra giao diện -> thấy trang chủ của shopee
    2.
        ![alt text](screenshot/image.png)
        Status code của request đầu tiên: 200 (Thành công và trả về kết quả)
        ![alt text](screenshot/image-1.png)
        Tổng thời gian load trang: 1.46 giây
        ![alt text](screenshot/image-2.png)
        Request trả về file CSS trong đó : status code: 200 (Thành công và trả về kết quả), thời gian thực hiện của request: 73ms
CÂU A2:
    +Tại sao trang web bị Google đánh giá SEO thấp?
        Vì đoạn code sử dụng thẻ <div> cho mọi thứ thay vì semantic tags.
        -> Google không thể hiểu cấu trúc trang -> xếp hạng thấp trong kết quả tìm kiếm
    + 4 lỗi semantic:
        -Lỗi 1: dòng <div class="header"> thay vì <header> khiến cho google không thể nhận diện phần header
        -Lỗi 2: dòng <div class="menu"> và <div><a> thay vì <nav>
            + Vấn đề: Menu không được đánh dấu sementic 
            + Sửa: <nav><ul><li><a>...</a></li></ul></nav>
        -Lỗi 3: dòng <div class="main"> thay vì <main>
            + Vấn đề: Nội dung chính không được xác định
            + Sửa: <main>...</main>
        -Lỗi 4: <div class="product"> + <div class="title"> thay vì <article> + <h2>
            - Vấn đề: Sản phẩm không cấu trúc đúng, không hỗ trợ schema.org/Product 
    -Đoạn code sau khi đã sửa: 
        <header>
            <div class="logo">ShopTLU</div>
            <nav>
            <ul>
                <li><a href="/">Trang chủ</a></li>
                <li><a href="/products">Sản phẩm</a></li>
            </ul>
            </nav>
        </header>   

        <main> 
            <article class="product">
                <h2>iPhone 16 Pro</h2>
                <figure><img src="iphone.jpg" alt="..."></figure>
                <p class="price">25.990.000đ</p>
            </article>
        </main>

        <footer> 
             <p>&copy; 2026 ShopTLU</p>
        </footer>

CÂU A3:
    ![alt text](screenshot/text_art.jpg)

    Giải thich:
    - <div>: Chiếm cả dòng có thể xuống dòng mới và điều chỉnh chiều rộng,dài
    - <span>: Chỉ chiếm phần nội dung,nằm cùng dòng với nhau
    - <strong> : Chỉ chiếm phần nội dung,nằm cùng dòng với nhau,in đậm để nhấn mạnh nội dung

CÂU B3: PHẦN B-THỰC HÀNH CODE
    Lỗi 1: Dòng 136 — <!DOCTYPE> không đầy đủ
       Cách sửa: <!DOCTYPE html>

    Lỗi 2: Dòng 137 — <html> thiếu lang="vi"
        Cách sửa: <html lang="vi">

    Lỗi 3: Dòng 139 — <title> thiếu thẻ đóng
        Cách sửa: <title>Trang web</title>

    Lỗi 4: Dòng 140 — charset viết sai (utf8 -> UTF-8)
        Cách sửa: <meta charset="UTF-8">

    Lỗi 5: Dòng 143 — <h1> đóng tag sai 
        Cách sửa: <h1>Welcome to ShopTLU</h1>

    Lỗi 6: Dòng 147 — <a> thiếu thẻ đóng  
        Cách sửa: <a href="home">Trang chủ</a>

    Lỗi 7: Dòng 155 — <img> không có dấu ngoặc kép quanh src
        Cách sửa: <img src="iphone.jpg">

    Lỗi 8: Dòng 157 — <b> và </p> bị nhầm vị trí 
        Cách sửa: <p>Giá: <b>25.990.000đ</b></p>

    Lỗi 9: Dòng 162-171 — <table> thiếu <thead>, <tbody>
        Cách sửa:  <table>
                        <thead>
                            <tr>
                                <td>Tên</td>
                                <td>Giá</td>
                            </tr>
                        </thead>

                        <tbody>
                            <tr>
                                <td>iPhone</td>
                                <td>25tr</td>
                            </tr>
                        </tbody>
                    </table>

    Lỗi 10: Dòng 175 — Có 2 thẻ <main> 
            Cách sửa:   <aside>
                            <p>Sidebar content</p>
                        </aside>

    Lỗi 11: Dòng 180 — <p> trong <footer> không đóng tag
            Cách sửa: <p>Copyright 2026</p>
