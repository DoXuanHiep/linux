# Managing groups users

## I/Managing users

### 1.Users

   - user phân thành 2 loại chính là *supperuser(root)* và *normaluser* .

Đường dẫn:  
- ` /etc/passwd ` là file lữu trữ thông tin users.

### 2.Thông tin về file ` /etc/passwd `

``` root:x:0:0:root:/root:/bin/bash

hiep:x:500:500:doxuanhiep:/home/hiep:/bin/bash ```

- Trong file chứa các người dùng có 7 trường mỗi trường ngăn cách nhau bởi dấu ` : ` .

- **Thông tin về từng trường**.

   - Trường đầu của users là **username(tên user) .** 

   - Trường thứ hai của users là mật khẩu đã được ẩn đi bằng chữ *x* .

   - Trường thứ ba của users là **UID(user id)** . *Đây chính là phân biệt xem user này thuộc loại supperuser hay normaluser* .

   - Trường thứ tư của users là **GID(group id)** .   

   - Trường thứ năm của users là **user id infor** . *Đây là trường cho phép người dùng có thể thêm thông tin về mình* .

   - Trường thứ sáu của user là **home directory** . *Đây là trường nói về đường dẫn tuyệt đối đến thư mục home* . 

   - Trường thứ bảy của user là  **command/shell** . *Đây là trường nói về command/shell(/bin/bash)* . 

### 3.Mật khẩu user

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

   - Trường đầu nói về **username(tên người dùng)**.

   - Trường thứ hai nói về mật khẩu của user đã được mã hóa. Những user nào mật khẩu  có kí tự là ` * ` là đã chết, chứa kí tự ` !! ` thì chưa tạo mật khẩu.

   - Trường thứ ba nói về lần đặt mật khẩu cuối cùng của user có số ngày tính bằng ` thời gian đặt mật khẩu trừ đi ngày 1 tháng 1 năm 1970 ` .

   - Trường thứ tư nói về số ngày tối thiểu giữa hai lần thay đổi mật khẩu.

   - Trường thứ năm nói về số ngày lớn nhất trước khi mật khẩu của bạn bị vô hiệu hóa.

   - Trường thứ sáu nói về số ngày trước khi mặt khẩu của bạn bị vô hiệu hóa. Và bạn sẽ được cảnh báo buộc phải thay đổi mật khẩu.

### 4.Groups

- Mỗi người sử dụng có thể thuộc về nhiều nhóm.

   - Mỗi nhóm = tên nhóm + danh sách các thành viên.

   - Khả năng chia sẻ file giữa các thành viên trong nhóm.

- Đường dẫn tới file quản lí group.

` /etc/group `

``` 
root:x:0:
hiep:x:500:
```

- Trong file chứa thông tin về người dùng có bốn trường thông tin được ngăn cách nhau bởi dấu ` : ` .

- **Thông tin về từng trường.** 

   - Trường thứ nhất nói về *groupname(tên nhóm)*.

   - Trường thứ hai nói về mật khẩu của group đã được ẩn đi bởi chữ ` x ` .

   - Trường thứ ba nói về GID.

   - Trường thứ tư nói về những người có trong nhóm đó.    

   
   




