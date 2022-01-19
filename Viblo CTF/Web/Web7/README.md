Link: http://172.104.49.143:1312/

Bài này để bắt đầu ta sẽ search thử file `robots.txt` thì được 

![image](https://user-images.githubusercontent.com/72268643/150124717-b590ed94-361a-4b0e-86c1-92e4adeadb21.png)

Search tiếp với file `index.abc` ta có được sourcecode

Đại khái hàm này sẽ có 1 hàm `ereg()` lọc các kí tự đặc biệt và chỉ cho phép chữ và số được nhập vào.

Tuy nhiên ở dưới lại có hàm in ra flag và bắt nhập và `^_^` :) 

![image](https://user-images.githubusercontent.com/72268643/150125367-5936a390-af82-4c77-bf71-eae641951049.png)

Khi search thông tin về hàm `ereg()`, ta gặp [không ít bài đăng](https://stackoverflow.com/questions/13580784/deprecated-function-ereg-is-deprecated) khuyên không nên dùng và thay thế bằng hàm `preg_replace()` từ phiên bản PHP 5.3.0 vì 

Vậy hướng là sẽ là bypass hàm `ereg()` để có thể nhập vào kí tự đặc biệt. Search `Bypass ereg php` ta thấy được vấn đề ở bài đầu tiên

![image](https://user-images.githubusercontent.com/72268643/150126414-30f405ed-8740-455e-8d63-cdf8652e80e6.png)

Vậy ta truyền password qua phương thức POST với giá trị: `A%00^_^` 

![image](https://user-images.githubusercontent.com/72268643/150127017-697cac79-0dc6-4188-9a48-75e1f551211f.png)

**Flag{POISON_NULL_BYTE}**
