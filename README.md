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
    "code": 0,
    "message": "ok"
}
```
## 获取角色 9/10
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
## 获取民族 9/10
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
## 员工基本信息 9/10
### 链接: POST    /users
#### 参数
```
string :name  #名称
integer :gender #性别
integer :nation_id #民族
string :id_card_number #身份证号码
datetime :birthdate #出生日期
string :domicile_place #户籍所在地
string :tel #练习电话
string :contact_address #联系地址
integer :company_id #当前单位
integer :wil_go_company_id #调往单位
integer :insurance_id #保险
integer :recruitment_project_id #招聘项目
integer :recruiter_id #招聘专员类型
integer :recruiter_user_id #招聘专员
datetime :dispatch_at #派遣时间
datetime :contract_start_date #合同开始时间
datetime :contract_end_date #合同结束时间
integer :contract_id #合同类型
string :accumulation_fund #公积金
string :accumulation_fund_number #公积金账户
string :bank_of_deposit #开户行
string :bank_card_number #银行卡号
boolean :work_type #员工状态

string :id_card_pic #身份证照片
string :bank_card_pic #银行卡照片
string :labor_contract_pic #劳动合同
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```
## 员工基本信息 9/10
### 链接: GET    /users/recruiter_users
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```
## 获取合同类型 9/10
### 链接: GET    /contracts
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "contracts": [
        {
            "id": 1,
            "name": "劳务派遣",
            "created_at": "2018-09-10T07:56:14.024Z"
        },
        {
            "id": 2,
            "name": "劳务外包",
            "created_at": "2018-09-10T07:56:14.028Z"
        }
    ]
}
```
## 获取保险类型 9/10
### 链接: GET    /insurances
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "insurances": [
        {
            "id": 1,
            "name": "社保",
            "created_at": "2018-09-10T07:56:14.040Z"
        },
        {
            "id": 2,
            "name": "商业保险",
            "created_at": "2018-09-10T07:56:14.044Z"
        }
    ]
}
```

## 获取招聘专员类型 9/10
### 链接: GET    /recruiters
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "recruiters": [
        {
            "id": 1,
            "name": "自有门店",
            "created_at": "2018-09-10T07:56:14.057Z"
        },
        {
            "id": 2,
            "name": "加盟店",
            "created_at": "2018-09-10T07:56:14.061Z"
        },...
    ]
}
```
