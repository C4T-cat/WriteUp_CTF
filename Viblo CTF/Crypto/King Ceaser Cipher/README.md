Chúng ta có: 

![image](https://user-images.githubusercontent.com/72268643/149792507-26573ed5-6dd0-45e2-9e7b-80b61464ba2b.png)

Để bắt đầu decode thì chúng ta sẽ decode phần số trước (hoặc chữ cũng được). 

![image](https://user-images.githubusercontent.com/72268643/149793496-fc8e2d2e-b492-4e94-9570-f2ad07d1626f.png)

Tiếp đến là decode phần chữ. Bảng chữ cái của chúng ta sẽ là: **abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ**

![image](https://user-images.githubusercontent.com/72268643/149794865-837e3526-807d-4dce-9de7-6fa4e6f03934.png)

Do không nhập được chữ in thường vào bảng chữ cái nên chú ý với key là 48 (dịch sang phải 4 kí tự) thì các chữ **W, X, Y, Z** sẽ trở thành các chữ in thường lần lượt là **a, b, c, d**

Flag cuối cùng là: **Flag{e44a584d495e62d44b78579a7480e633}**
