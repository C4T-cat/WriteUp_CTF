Đầu tiên, chúng ta có 1 trang web qua đường link: http://172.104.49.143:1335

![image](https://user-images.githubusercontent.com/72268643/150055518-c9018cce-c803-4bf0-a83b-0d72c6b31d15.png)

Để ý thấy tuy trang web không có gì nhưng ở URL chúng ta có một kí tự sau đường dẫn 

![image](https://user-images.githubusercontent.com/72268643/150056212-9a0fe77b-d338-43cc-8da0-b5ace6d170c1.png)

Sau khi reload lại, chúng ta lại được một kí tự khác

![image](https://user-images.githubusercontent.com/72268643/150056289-aeb13d66-0352-4d0a-b42c-78bfe855781e.png)

Để kiểm tra các request, ta check Inspect/Network và thấy các tệp tin chữ cái được liên tục chuyển hướng 7 lần và dẫn đến tệp cuối cùng được hiển thị

![image](https://user-images.githubusercontent.com/72268643/150059131-573e70af-5c8f-4574-9662-c63d8dd19860.png)

Vậy nên chúng ta sẽ sắp xếp chúng theo thời gian chúng được request và thấy xuất hiện chữ **'Flag{'**

![image](https://user-images.githubusercontent.com/72268643/150059283-049968f8-b16b-44d9-839e-f32ff896be93.png)

Do đó, chúng ta sẽ ghi các từ đó lại, reload trang web rồi check lại Network sẽ được các tệp tin chữ cái mới.

Làm vậy cho đến khi bạn thấy từ 'Flag' lặp lại (hình như không có dấu '}'), ta có được Flag là: **Flag{URI_is_Import@nT}**
