Chúng ta có đường link tới trang web: http://172.104.49.143:1318/

Sau khi tới trang web, chúng ta sẽ được 'mời' check sourcecode luôn :)

![image](https://user-images.githubusercontent.com/72268643/150061295-58d2faaf-edcb-4f6d-956a-ea181a643fc3.png)

Vấn đề chính nằm ở hàm PHP. Nếu ta truyền vào đúng giá trị cho biến `$what_you_actually_heard` (`HomNayOT_EmNhe`) thì ta sẽ chạy được hàm poor_you() vào có thể có flag

Nhưng, có 1 rào cản đó là sẽ có 1 bộ lọc trước khi truyền vào biến `$what_you_actually_heard`. Bộ lọc này sẽ xóa tất cả các chuỗi kí tự giống giá trị của biến `$what_you_dont_want_to_hear` 

![image](https://user-images.githubusercontent.com/72268643/150077000-08e94160-9b51-4e81-a671-9956f6281cb4.png)

Tuy nhiên, hàm này chạy như 1 vòng for, nó chỉ chạy 1 lần từ đầu đến cuối vào loại bỏ các chuỗi đó. Vậy nên nếu chúng ta truyền vào 1 chuỗi như `HomNayHomNayOT_EmNheOT_EmNhe`,

hàm `preg_replace()` sẽ chỉ loại bỏ chuỗi hoàn chỉnh ở giữa vào kết thúc, để lại cho chúng ta chuỗi còn lại là giá trị cần truyền vào.

![image](https://user-images.githubusercontent.com/72268643/150077311-259f9fee-f9cf-4daf-a21b-6c209d3d7e6f.png)

Flag là: **Flag{V4ng_4nh_cu0c_s0ng_m4}**
