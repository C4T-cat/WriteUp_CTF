Link: https://ctf.viblo.asia/puzzles/innocent-game-imgauhqefhq

Đầu tiên ta sẽ thử nhập vào chuỗi chữ số bất kì, ta có được thông báo: 

![image](https://user-images.githubusercontent.com/72268643/150154326-6e9bbad1-9957-4684-923a-56255fe35d72.png)

`Dấu ngăn cách không thể là kí tự chữ hoặc số hoặc là dấu '\'`. Vậy nên t sẽ thử nhập vào các dấu như `#$/` và được:

![image](https://user-images.githubusercontent.com/72268643/150165275-4f3a5c66-b4d6-4510-9a46-f15c22a3b889.png)

Search `No ending delimiter '/' found` ta thấy rằng cần thêm 1 cặp dấu `/ /` vào trước và sau biến cần thay đổi ([Đọc thêm](https://stackoverflow.com/questions/4634993/php-regular-expressions-no-ending-delimiter-found-in))

Ví dụ ta thay thế 4 icon đầu bằng chuỗi số 2 như sau:

![image](https://user-images.githubusercontent.com/72268643/150173520-8c294ab9-0358-43f1-89fa-a09489718322.png)

Kết quả:
![image](https://user-images.githubusercontent.com/72268643/150173469-bd3588bc-ad73-4131-a57b-b88e301e74c0.png)

Vấn đề còn lại là chúng ta cần khai thác hàm `preg_replace()`. Search `pre_replace() exploit` ta sẽ thấy [1 bài đăng viết về cách khai thác thông qua `/e`](https://captainnoob.medium.com/command-execution-preg-replace-php-function-exploit-62d6f746bda4)

vậy ta sẽ có thể cần thay thế icon bất kì bằng câu lệnh thực thi như `ls` và để vào trong dấu \` \` để php có thể thực thi

![image](https://user-images.githubusercontent.com/72268643/150179933-b171fdad-0309-400c-a0d6-19bad1c3a9d3.png)

Kết quả: 
![image](https://user-images.githubusercontent.com/72268643/150179972-6436f1bc-2267-4496-8ef5-6fa41ed3983d.png)

Vậy ta sẽ chạy thử file `index.php`

![image](https://user-images.githubusercontent.com/72268643/150180119-1a9a69ab-99b6-4c00-a299-4885333e23fa.png)

Kết quả: 
![image](https://user-images.githubusercontent.com/72268643/150180205-6f5f4eaa-3601-4616-9cf2-e72f3bb23588.png)

Check sourcecode, ta thấy được flag là: **Flag{preg_replacep_c4n7_b3_7h15_d4n63r0u5}**

![image](https://user-images.githubusercontent.com/72268643/150180350-4ad20385-d0d7-457a-8789-04ad8510baa7.png)
