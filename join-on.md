select * from "user" join post on post.user_id = "user".id;

![image](https://github.com/user-attachments/assets/8b3e45e7-59f1-40ea-8fa6-3f0f49f46d7a)


select "user".*, post.id, post.name as title, post.content, post.user_id from "user" join post on post.user_id = "user".id;

Câu lệnh SQL:

sql
Copy code
SELECT "user".*, 
       post.id, 
       post.name AS title, 
       post.content, 
       post.user_id 
FROM "user" 
JOIN post ON post.user_id = "user".id;
Giải thích chi tiết từng phần:
1. Mục đích
Câu lệnh này kết hợp (join) dữ liệu từ hai bảng "user" và post dựa trên mối quan hệ giữa:

Cột user_id trong bảng post (khóa ngoại).
Cột id trong bảng "user" (khóa chính).
Kết quả: Hiển thị dữ liệu từ bảng "user" và các thông tin liên quan trong bảng post.

2. Các thành phần chính
a. SELECT "user".*
"user".*: Lấy toàn bộ các cột từ bảng "user".
Ví dụ: Nếu bảng "user" có các cột id, name, email, password, age, thì tất cả các cột này sẽ được hiển thị trong kết quả.
b. post.id
Lấy cột id từ bảng post. Đây là ID của bài viết.
c. post.name AS title
Lấy cột name từ bảng post và gán nó một bí danh (alias) là title.
Trong kết quả, cột này sẽ được hiển thị với tên là title.
d. post.content
Lấy cột content từ bảng post. Đây là nội dung bài viết.
e. post.user_id
Lấy cột user_id từ bảng post. Đây là ID của người dùng đã viết bài.
3. FROM "user" JOIN post ON post.user_id = "user".id
JOIN: Kết hợp hai bảng dựa trên điều kiện.
ON post.user_id = "user".id:
Điều kiện này đảm bảo rằng:
Bản ghi trong bảng post sẽ được kết hợp với bản ghi trong bảng "user" khi giá trị của post.user_id bằng giá trị của "user".id.
Điều này đảm bảo bạn chỉ lấy những bài viết có liên kết với người dùng hợp lệ.

![image](https://github.com/user-attachments/assets/0462ec5d-a4c8-4058-9876-f703aa5a873e)

Lời khuyên
Nếu bảng có nhiều cột không cần thiết, hạn chế dùng * để tránh lấy dư dữ liệu.
Bạn có thể chọn cụ thể các cột cần thiết, ví dụ:
sql
Copy code
SELECT "user".name AS user_name, 
       "user".email, 
       post.name AS post_title, 
       post.content 
FROM "user" 
JOIN post ON post.user_id = "user".id;


