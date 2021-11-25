# WriteUp: 

Khi vào trang web, ta thấy được alert. Sau đó là 1 form login.

![image](https://user-images.githubusercontent.com/72268643/143457671-ab87dda5-235d-49b1-8df4-89747a2d5162.png)

Check source code form login ta thấy được 1 tài khoản

![image](https://user-images.githubusercontent.com/72268643/143457717-3ef28857-cc62-4227-aa2d-174953b380dc.png)

Đăng nhập thành công bằng tài khoản đó tuy nhiên do không đúng token nên không có gì. 

Chúng ta thử kiểm tra cookies thì thấy có cookies token. Do đó hướng làm là thay đổi token value.

![image](https://user-images.githubusercontent.com/72268643/143457777-dae8b34e-1570-42e8-9c70-e68e8618635f.png)

Chúng ta sẽ quay lại và thử kiểm tra hàm js đã alert ra thông báo.

![image](https://user-images.githubusercontent.com/72268643/143459019-ee44c827-f0e6-4b7c-8dd1-104700125611.png)

Kéo xuống cuối chúng ta sẽ có được token **1_4m_4n_3mpl0y33**.

![image](https://user-images.githubusercontent.com/72268643/143458915-d9d37fe9-a491-4dcf-b7a9-b79b2bd7c263.png)

Có được token, chúng ta login như bình thường và thay đổi token value rồi reload trang web.

![image](https://user-images.githubusercontent.com/72268643/143459149-d91b2904-03a7-4902-bc30-bbccf9b5e798.png)

Flag là: **DSPH{y0u_h4ckedd_DspH}**
