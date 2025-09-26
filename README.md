npm install 
-Khởi chạy server App : node app.js

ĐĂNG KÝ trường hợp thành công
Method: POST
URL: http://localhost:3000/auth/register
Body (x-www-form-urlencoded): 
Data
username: admin
password: 12345
Kết quả: 
<h2>Login</h2>
<form action="/login" method="POST">
  <input type="text" name="username" placeholder="Username" required /><br>
  <input type="password" name="password" placeholder="Password" required /><br>
  <button type="submit">Login</button>
</form>
<a href="/register">Register</a>

![alt text](public/image/1.png)
check in website
![alt text](public/image/10.png)
![alt text](public/image/14.png)
Check in Database
![alt text](public/image/2.png)
![alt text](public/image/11.png)
==============================================
ĐĂNG KÝ trường hợp không thành công
Method: POST
URL: http://localhost:3000/auth/register
Body (x-www-form-urlencoded): 
Data:
username: admin
password: 12345

Kết quả: 
Error: E11000 duplicate key error collection: passportAuth.users index: username_1 dup key: { username: "admin" }

![alt text](public/image/3.png)
![alt text](public/image/16.png)

==============================================
Đăng nhập thành công
Method: POST
URL: http://localhost:3000/login
Body: x-www-form-urlencoded
Data:
username: admin
password: 12345
Kết quả: 
<h2>Welcome admin</h2>
<a href="/logout">Logout</a>

![alt text](public/image/4.png)
![alt text](public/image/5.png)
![alt text](public/image/12.png)
![alt text](public/image/13.png)

==============================================
Đăng nhập không thành công
Method: POST
URL: http://localhost:3000/login
Body: x-www-form-urlencoded
Data:
username: admin
password: 123456
Kết quả: 
<h2>Login</h2>
<form action="/login" method="POST">
  <input type="text" name="username" placeholder="Username" required /><br>
  <input type="password" name="password" placeholder="Password" required /><br>
  <button type="submit">Login</button>
</form>
<a href="/register">Register</a>

![alt text](public/image/6.png)
![alt text](public/image/15.png)
==============================================
Truy cập profile
Method: GET
URL: http://localhost:3000/profile
Kết quả: 
<h2>Welcome admin</h2>
<a href="/logout">Logout</a>

![alt text](public/image/7.png)
![alt text](public/image/13.png)

==============================================
Đăng xuất
Method: GET
URL: http://localhost:3000/logout
kết quả:
<h2>Login</h2>
<form action="/login" method="POST">
  <input type="text" name="username" placeholder="Username" required /><br>
  <input type="password" name="password" placeholder="Password" required /><br>
  <button type="submit">Login</button>
</form>
<a href="/register">Register</a>

![alt text](public/image/8.png)

==============================================
Truy cập profile sau khi logout
Method: GET 
URL: http://localhost:3000/profile
Kết quả: 
<h2>Login</h2>
<form action="/login" method="POST">
  <input type="text" name="username" placeholder="Username" required /><br>
  <input type="password" name="password" placeholder="Password" required /><br>
  <button type="submit">Login</button>
</form>
<a href="/register">Register</a>

![alt text](public/image/9.png)

