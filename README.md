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
## 获取角色
### 链接: GET    /roles
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "roles": [
        {
            "id": 1,
            "name": "总经理",
            "created_at": "2018-09-10T01:25:42.857Z"
        },
        {
            "id": 2,
            "name": "业务经理",
            "created_at": "2018-09-10T01:25:42.860Z"
        },...
    ]
}
```
## 获取民族
### 链接: GET    /nations
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "nations": [
        {
            "id": 1,
            "name": "汉族",
            "created_at": "2018-09-10T02:38:56.921Z"
        },
        {
            "id": 2,
            "name": "蒙古族",
            "created_at": "2018-09-10T02:38:56.925Z"
        },...
    ]
}
```
