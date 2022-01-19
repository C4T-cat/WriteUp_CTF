Link: http://172.104.49.143:1303/

Như thường lệ, Check source code ta thấy có comment `<!-- index.phps -->`, sau đó tìm file index.phps ta được: 

![image](https://user-images.githubusercontent.com/72268643/150095612-26fcf83c-d976-4588-803b-168aa1ada966.png)

Ở đây ta thấy biến `$flag` sẽ in ra giá trị của biến `$key` (có vẻ là flag) nếu đạt đủ điều kiện (`$value` khác chuỗi rỗng và hàm giá trị `$value` bằng giá trị `$key`)

Khả năng cao nếu nhập đúng giá trị biến `$key` (khả năng cao) là flag thì sẽ khá khó. Vậy nên chúng ta sẽ chuyển hướng xử lý tới hàm `strcmp()`

Để hàm đó trả về giá trị 0, ta có thể truyền vào 1 mảng để so sánh với 1 chuỗi (still searching)

(continue...)
