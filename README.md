# 文档
## 登录
### 链接: POST   /authentication
#### 参数
```
body:
"tel":"15000000000"
"password":"15000000000"
```
#### 返回值
```
{
    "token": "eyJhbGciOiJub25lIn0.eyJ1c2VyX2lkIjoxLCJleHAiOjE1MzYzMTQzMzF9."
}
```
## 获取用户列表
### 链接: GET    /users
#### 参数
```
headers:
"Authorization":"eyJhbGciOiJub25lIn0.eyJ1c2VyX2lkIjoxLCJleHAiOjE1MzYzMTQzMzF9."
```
#### 返回值
```
{
    "token": "eyJhbGciOiJub25lIn0.eyJ1c2VyX2lkIjoxLCJleHAiOjE1MzYzMTQzMzF9."
}
```
