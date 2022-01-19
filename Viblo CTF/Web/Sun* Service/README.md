Link: http://172.104.49.143:1317/

![image](https://user-images.githubusercontent.com/72268643/150102694-4bb05418-a42e-4b97-bb67-f88f6d1815bb.png)

Làm như hướng dẫn, ta được kết quả là câu lệnh ping tới trang Google.com

![image](https://user-images.githubusercontent.com/72268643/150102878-c337c336-4086-4013-8322-5fa44e50de97.png)

Để thử xem trên đó có những file gì, ta thực hiện câu lệnh `; ls` (dấu `;` để ngăn cách với câu lệnh trước) thì ta được

![image](https://user-images.githubusercontent.com/72268643/150104705-fb508ec5-4e8d-43eb-9293-2a6f9e6f6b75.png)

Hmmm, thử với `;ls` xem 

![image](https://user-images.githubusercontent.com/72268643/150104870-ffa6607d-5a3b-4966-9861-6d090a31a102.png)

Oke, thử chạy hàm `index.php` với câu lệnh `cat index.php` thì ta lại được như trên:

![image](https://user-images.githubusercontent.com/72268643/150105235-713f1c02-5331-4b55-a233-a4b466aa8bea.png)

Hmm, có lẽ dấu cách `' '` đã ngăn cản câu lệnh thực hiện :( 

Oke vậy cần tìm câu lệnh đọc file mà không có khoảng trắng. Thử search **bypass space cat command** ta sẽ gặp được [1 bài ở trên Viblo nó về điều đó](https://viblo.asia/p/bypass-os-command-injection-XL6lA4rNZek)

Ta thấy được có luôn cái cần tìm

![image](https://user-images.githubusercontent.com/72268643/150106429-40977aba-769d-4a80-80c9-5ac1d1eb3ab8.png)

Sau đó thử các câu lệnh tương tự, câu lệnh `;cat${IFS}index.php` hoạt động và ta có được: 

![image](https://user-images.githubusercontent.com/72268643/150106767-8bd2af57-5a1b-4215-a552-b24f821517a7.png)

Check sourcecode ta sẽ thấy được flag: 

![image](https://user-images.githubusercontent.com/72268643/150106911-20abdc1c-0a5e-4459-8996-81e2f7780734.png)

Vậy flag là: **Flag{Th1s_1s_4n_3asY_FL4G_R1ght?}**
