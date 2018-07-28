# Managing groups users

## I/Managing users

### 1.Users

<ul><li>user phân thành 2 loại chính là *supperuser(root)* và *normaluser*.</li></ul>

Đường dẫn:  
<ul>` /etc/passwd ` là file lữu trữ thông tin users.</ul>

### 2.Thông tin về file ` /etc/passwd `

``` root:x:0:0:root:/root:/bin/bash

hiep:x:500:500:doxuanhiep:/home/hiep:/bin/bash ```

- Trong file chứa các người dùng có 7 trường mỗi trường ngăn cách nhau bởi dấu ` : ` .

- **Thông tin về từng trường**.

<ul>
<li>Trường đầu của users là **username(tên user).** </li>

<li>Trường thứ hai của users là mật khẩu đã được ẩn đi bằng chữ *x* .</li> 

<li>Trường thứ ba của users là **UID(user id)**. *Đây chính là phân biệt xem user này thuộc loại supperuser hay normaluser*. </li>

<li>Trường thứ tư của users là **GID(group id)**. </li>  

<li>Trường thứ năm của users là **user id infor**. *Đây là trường cho phép người dùng có thể thêm thông tin về mình*. </li>

<li>Trường thứ sáu của user là **home directory**. *Đây là trường nói về đường dẫn tuyệt đối đến thư mục home*. </li>

<li>Trường thứ bảy của user là  **command/shell**. *Đây là trường nói về command/shell(/bin/bash)*. </li>
</ul>

### Mật khẩu user

- Đường dẫn: ` /etc/shadow `

``` 
root:$6$elt9KOt1$eDLOKG89.ideC5D8vT5w6AT7/UxyoYXuBrTIa5r3EVTMn78e/.orHkWrgeKWxi9DO860T2wPoabfKhMumXKfC0:17692:0:99999:7:::
bin:*:17246:0:99999:7:::
nslcd:!!:17256::::::
hiep:$6$KJ8Cid.C7eM926D9$0hl1ZBId0IhGeJGsbyHWILQ9o30BHNQhEVAdXCm9GOU32qdu1caWXxMbIBAEH.iBAhKwBu2rCkorQKZTW6fJC0:17683:0:99999:7::: 
```

- Trong file ` /etc/shadow ` lưu trữ thông tin về mật khẩu của users.

- Trong file chứa thông tin về người dùng có tổng cộng 9 trường thông tin dược ngăn cách với nhau bởi dấu ` : ` .

- **Thông tin về tường trường.**

<ul>
   <li> Trường đầu nói về **username(tên người dùng)**.</li>
   <li>Trường thứ hai nói về mật khẩu của user đã được mã hóa. Những user nào mật khẩu  có kí tự là  là đã chết </li>
</ul>   




