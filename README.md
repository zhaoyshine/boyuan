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
## 员工基本信息 9/14
### 链接: POST    /employees
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

string :id_card_pic, array: true #身份证照片
string :bank_card_pic, array: true #银行卡照片
string :labor_contract_pic, array: true #劳动合同
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```
## 带队人员列表 9/14
### 链接: GET    /employees/recruiter_users
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": [],
    "meta": {
        "pagination": {
            "total_pages": 0,
            "current_page": 1,
            "next_page": null,
            "prev_page": null,
            "first_page": true,
            "last_page": false,
            "total_length": 0
        }
    }
}

```


## 带队人员下拉列表数据 9/14
### 链接: GET   /employees/drop_down_lists
#### 参数
```
```
#### 返回值
```
{
    "code": "0",
    "data": [
        {
            "id": 1,
            "name": null,
        }
    ]
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

## 创建单位协议 9/12
### 链接: POST   /agreements
#### 参数
```
integer :organization_id #单位名称
integer :customer_person_id #客服专员
datetime :sign_time #协议签订时间
datetime :file_start #协议时期
datetime :file_end #协议结束
string :file_last #合同期限
text :file_content #协议内容
text :extra_content #协议内容

string :file, array: true #相关附件
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 更新单位协议 9/12
### 链接: PATCH   /agreements/:id
#### 参数
```
:id: agreement_id
integer :organization_id #单位名称
integer :customer_person_id #客服专员
datetime :sign_time #协议签订时间
datetime :file_start #协议时期
datetime :file_end #协议结束
string :file_last #合同期限
text :file_content #协议内容
text :extra_content #协议内容

string :file, array: true #相关附件
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 单位协议列表 9/12
### 链接: GET    /agreements
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": [],
    "meta": {
        "pagination": {
            "total_pages": 0,
            "current_page": 1,
            "next_page": null,
            "prev_page": null,
            "first_page": true,
            "last_page": false,
            "total_length": 0
        }
    }
}

```

## 单位协议详细信息 9/12
### 链接: GET    /agreements/:id
#### 参数
```
:id:agreement_id
```
#### 返回值
```
{
    "code": "0",
    "data": "agreement info..."
}

```

## 创建单位 9/12
### 链接: POST   /organizations
#### 参数
```
string :company_name #单位名称 
integer :contract_id #服务类型
integer :customer_person_id #客服专员
string :company_type #公司性质
string :work_type #公司性质
string :company_size #企业规模
string :company_address #企业地址
string :lawer_person #法人代表
string :lawer_contact #联系方式
string :specile_person #专事联系人
string :specile_contact #联系方式
integer :role_id #所属部门
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 更新单位 9/12
### 链接: PATCH   /organizations/:id
#### 参数
```
:id: organization_id
string :company_name #单位名称 
integer :contract_id #服务类型
integer :customer_person_id #客服专员
string :company_type #公司性质
string :work_type #公司性质
string :company_size #企业规模
string :company_address #企业地址
string :lawer_person #法人代表
string :lawer_contact #联系方式
string :specile_person #专事联系人
string :specile_contact #联系方式
integer :role_id #所属部门
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 单位列表 9/12
### 链接: GET    /organizations
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": [],
    "meta": {
        "pagination": {
            "total_pages": 0,
            "current_page": 1,
            "next_page": null,
            "prev_page": null,
            "first_page": true,
            "last_page": false,
            "total_length": 0
        }
    }
}

```

## 单位详细信息 9/12
### 链接: GET    /organizations/:id
#### 参数
```
:id:organization_id
```
#### 返回值
```
{
    "code": "0",
    "data": "organization info..."
}

```


## 创建招聘项目 9/12
### 链接: POST   /recruitment_projects
#### 参数
```
integer :organization_id #单位名称
string :name #招聘主题
string :recruiting_numbers #招聘人数
string :treatment_hour #每小时的待遇
string :age_range #年龄要求
string :gender_requirement #性别要求
integer :contract_id #服务类型
string :position_statement #岗位职责
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 更新招聘项目 9/12
### 链接: PATCH   /recruitment_projects/:id
#### 参数
```
:id: recruitment_project_id
integer :organization_id #单位名称
string :name #招聘主题
string :recruiting_numbers #招聘人数
string :treatment_hour #每小时的待遇
string :age_range #年龄要求
string :gender_requirement #性别要求
integer :contract_id #服务类型
string :position_statement #岗位职责
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 招聘项目列表 9/12
### 链接: GET    /recruitment_projects
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": [],
    "meta": {
        "pagination": {
            "total_pages": 0,
            "current_page": 1,
            "next_page": null,
            "prev_page": null,
            "first_page": true,
            "last_page": false,
            "total_length": 0
        }
    }
}

```

## 招聘项目详细信息 9/12
### 链接: GET    /recruitment_projects/:id
#### 参数
```
:id:recruitment_project_id
```
#### 返回值
```
{
    "code": "0",
    "data": "recruitment project info..."
}

```


## 创建系统用户 9/12
### 链接: POST   /users
#### 参数
```
:name
:tel
:role_id
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 更新系统用户 9/12
### 链接: PATCH   /users/:id
#### 参数
```
:id: user_id
:name
:tel
:role_id
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 系统用户重置密码 9/12
### 链接: POST   /users/reset_pwd
#### 参数
```
:tel
:password 用户密码
:password_new 新密码
:password_new_confirmation 确认密码
```
#### 返回值
```
{code: 0, message: "ok"}
```

## 用户未读消息 9/12
### 链接: POST   /users/unread_count
#### 参数
```
```
#### 返回值
```
{
    "code": "0",
    "count": "0"
}
```


## 单位下拉列表数据 9/14
### 链接: GET   /organizations/drop_down_lists
#### 参数
```
```
#### 返回值
```
{
    "code": "0",
    "data": [
        {
            "id": 1,
            "company_num": null,
            "company_name": "上海穆际"
        }
    ]
}
```

## 招聘项目下拉列表数据 9/14
### 链接: GET   /recruitment_projects/drop_down_lists
#### 参数
```
```
#### 返回值
```
{
    "code": "0",
    "data": [
        {
            "id": 1,
            "name": "",
        }
    ]
}
```

## 员工续签合同 9/14
### 链接: POST   /employees/renew_contract
#### 参数
```
employee_id
contract_start_date
contract_end_date
string :labor_contract_pic, array: true #劳动合同
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 员工内部流转 9/14
### 链接: POST   /employees/interior_circulation
#### 参数
```
employee_id 
wil_go_company_id #调往的单位
remark
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 内部流转列表 9/14
### 链接: GET   /interior_circulations
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": [],
    "meta": {
        "pagination": {
            "total_pages": 0,
            "current_page": 1,
            "next_page": null,
            "prev_page": null,
            "first_page": true,
            "last_page": false,
            "total_length": 0
        }
    }
}
```


## 创建带队人员 9/14
### 链接: POST   /employees/recruiter
#### 参数
```
string :name  #名称
string :gender  #性别
string :id_card_number #身份证号码
string :tel #练习电话
integer :recruiter_id #招聘专员类型
string :bank_of_deposit #开户行
string :bank_card_number #银行卡号

string :id_card_pic, array: true #身份证照片
string :bank_card_pic, array: true #银行卡照片
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```
