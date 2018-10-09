# 文档

## 炫酷的锚点
- [登录](#登录)
- [获取角色](#获取角色)
- [获取民族](#获取民族)
- [员工列表](#员工列表)
- [系统员工列表](#系统员工列表)
- [薪资项目列表](#薪资项目列表)
- [薪资项目下拉列表](#薪资项目下拉列表)
- [创建薪资项目](#创建薪资项目)
- [更新薪资项目](#更新薪资项目)
- [企业工资列表](#企业工资列表)
- [创建企业工资](#创建企业工资)
- [更新企业工资](#更新企业工资)
- [社保新增人员](#社保新增人员)
- [公司人员列表](#公司人员列表)
- [公司人员下拉列表数据](#公司人员下拉列表数据)
- [购买社保](#购买社保)
- [在保人员列表](#在保人员列表)
- [停保人员列表](#停保人员列表)
- [人员停保操作](#人员停保操作)
- [社保变更记录](#社保变更记录)
- [社保缴费记录](#社保缴费记录)
- [社保变更](#社保变更)
- [已读消息](#已读消息)
- [未读消息](#未读消息)
- [设置未读消息成为已读](#设置未读消息成为已读)
- [删除消息](#删除消息)
- [招聘项目人员列表](#招聘项目人员列表)
- [批量导入公司](#批量导入公司)
- [七牛js-sdk上传文件获取token接口](#七牛js-sdk上传文件获取token接口)
- [七牛js-sdk下载文件获取token接口](#七牛js-sdk下载文件获取token接口)
- [公司获取招聘项目列表](#公司获取招聘项目列表)
- [公司获取招聘项目下拉列表](#公司获取招聘项目下拉列表)
- [批量导入公司](#批量导入公司)
- [更新员工基本信息](#更新员工基本信息)
- [人员离职操作](#人员离职操作)
- [更新带队人员](#更新带队人员)
- [更新带队人员](#更新带队人员)
- [材料列表](#材料列表)
- [材料用途](#材料用途)
- [新建材料](#新建材料)
- [更新材料](#更新材料)
- [带队人员的员工列表](#带队人员的员工列表)
- [社保变更列表](#社保变更列表)
- [企业工资表的人员列表](#企业工资表的人员列表)
- [企业工资表导出](#企业工资表导出)
- [企业工资表导入](#企业工资表导入)
- [todo-员工](#todo-员工)
- [todo-保险](#todo-保险)
- [todo-薪资](#todo-薪资)
- [todo-单位](#todo-单位)
- [删除单位协议](#删除单位协议)
- [删除员工](#删除员工)
- [删除单位](#删除单位)
- [删除单位招聘项目](#删除单位招聘项目)




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
## 员工基本信息
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
## 带队人员列表
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


## 带队人员下拉列表数据
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


## 获取合同类型
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
## 获取保险类型
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

## 获取招聘专员类型
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

## 创建单位协议
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

## 更新单位协议
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

## 单位协议列表
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

## 单位协议详细信息
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

## 创建单位
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

## 更新单位
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

## 单位列表
### 链接: GET    /organizations
#### 参数
```
optional! :company_name
optional! :customer_person_id
optional! :company_type
optional! :work_type
optional! :company_size
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

## 单位详细信息
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


## 创建招聘项目
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

## 更新招聘项目
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

## 招聘项目列表
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

## 招聘项目详细信息
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


## 创建系统用户
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

## 更新系统用户
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

## 系统用户重置密码
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

## 用户未读消息
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


## 单位下拉列表数据
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

## 招聘项目下拉列表数据
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

## 员工续签合同
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


## 员工内部流转
### 链接: POST   /employees/interior_circulation
#### 参数
```
employee_id 
diao_wang_date #调往时间
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


## 人员离职操作
### 链接: POST   /employees/leave_office_employees
#### 参数
```
integer :employee_id
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 内部流转列表
### 链接: GET   /interior_circulations
#### 参数
```
optional! :company_id
optional! :wil_go_company_id
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


## 创建带队人员
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


## 更新带队人员
### 链接: PATCH   /employees/recruiter_update
#### 参数
```
id
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


## 客户总数
### 链接: GET   /statistic/organizations_count
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "count": "0"
}
```


## 员工总数
### 链接: GET   /statistic/employees_count
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "count": "0"
}
```


## 在职员工总数
### 链接: GET   /statistic/active_employees_count
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "count": "0"
}
```


## 系统人员下拉列表数据
### 链接: GET   /users/drop_down_lists
#### 参数
```
role_id 
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


## 员工列表
### 链接: GET   /employees
#### 参数
```
optional! :gender
optional! :state
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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

## 系统员工列表
### 链接: GET    /users
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


## 薪资项目列表
### 链接: GET    /salary_projects
#### 参数
```
optional! :add_type
optional! :user_id
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

## 薪资项目下拉列表
### 链接: GET    /salary_projects/drop_down_lists
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

## 创建薪资项目
### 链接: POST   /salary_projects
#### 参数
```
integer :user_id
integer :weight #权重 从大到小排序
string :mark
string :name
boolean :add_type #加减项目
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 更新薪资项目
### 链接: PATCH   /salary_projects/:id
#### 参数
```
integer :user_id
integer :weight #权重 从大到小排序
string :mark
string :name
boolean :add_type #加减项目
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 企业工资列表
### 链接: GET    /payrolls
#### 参数
```
optional! :organization_id
optional! :recruitment_project_id
optional! :state
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



## 创建企业工资
### 链接: POST   /payrolls
#### 参数
```
integer :organization_id
integer :recruitment_project_id
string :sheet, array: true #表格
string :calculation #计算方式
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 更新企业工资
### 链接: PATCH   /payrolls/:id
#### 参数
```
integer :organization_id
integer :recruitment_project_id
string :sheet, array: true #表格
string :calculation #计算方式
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 社保新增人员
### 链接: GET    /insurances/new_insurances
#### 参数
```
optional! :insurance_id
optional! :state
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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


## 公司人员列表
### 链接: GET    /employees/organization_users
#### 参数
```
organization_id
optional! :state, values: %w[在职 离职]
optional! :insurance_id
optional! :recruitment_project_id
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


## 公司人员下拉列表数据
### 链接: GET   /employees/organization_user_drop_down_lists
#### 参数
```
organization_id
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


## 购买社保
### 链接: POST   /insurances/buy_insurances
#### 参数
```
integer :employee_id
string :insurance_platform
string :insurance_company
datetime :insurance_buy_date
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 在保人员列表
### 链接: GET    /insurances/exist_insurances
#### 参数
```
optional! :insurance_id
optional! :state
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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

## 停保人员列表
### 链接: GET    /insurances/stop_insurances
#### 参数
```
optional! :insurance_id
optional! :state
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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


## 人员停保操作
### 链接: POST   /insurances/stop_insurance_employees
#### 参数
```
integer :employee_id
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```

## 社保变更记录
### 链接: GET    /insurances/change_insurance_record
#### 参数
```
optional! :organization_id
optional! :insurance_id
optional! :to_organization_id
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


## 社保缴费记录
### 链接: GET    /insurances/payment_insurance_record
#### 参数
```
optional! :organization_id
optional! :insurance_id
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


## 社保变更
### 链接: POST    /insurances/change_insurances
#### 参数
```
employee_id
to_employee_id
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 已读消息
### 链接: GET    /notifications/read
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


## 未读消息
### 链接: GET    /notifications/unread
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



## 设置未读消息成为已读
### 链接: POST    /notifications/clean
#### 参数
```
ids, array: true
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 删除消息
### 链接: DELETE    /notifications/destroy_ids
#### 参数
```
ids, array: true
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```


## 招聘项目人员列表
### 链接: GET    /employees/recruitment_project_users
#### 参数
```
recruitment_project_id
optional! :state, values: %w[在职 离职]
optional! :insurance_id
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


## 批量导入公司
### 链接: POST    /organizations/add_organizations
#### 参数
```
file
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```


## 七牛js-sdk上传文件获取token接口
### 链接: GET    /token
#### 参数
```
```
#### 返回值
```
```


## 七牛js-sdk下载文件获取token接口
### 链接: POST    /downtoken
#### 参数
```
```
#### 返回值
```
```



## 公司获取招聘项目列表
### 链接: GET    /recruitment_projects/by_organization
#### 参数
```
organization_id
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

## 公司获取招聘项目下拉列表
### 链接: GET    /recruitment_projects/by_organization_drop_down_lists
#### 参数
```
organization_id
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

## 更新员工基本信息
### 链接: PATCH    /employees/:id
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



## 批量导入员工
### 链接: POST    /employees/add_employees
#### 参数
```
file
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```

## 材料列表
### 链接: GET    /pans
#### 参数
```
optional! :user_id
optional! :usage
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


## 材料用途
### 链接: GET    /pans/usage
#### 参数
```
```
#### 返回值
```
{
    "code": 0,
    "data": []
}
```


## 新建材料
### 链接: POST    /pans
#### 参数
```
string :name #名称
integer :user_id #上传人
string :usage #用途
string :desc #描述
string :file, array: true
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```


## 更新材料
### 链接: PATCH    /pans/:id
#### 参数
```
string :name #名称
integer :user_id #上传人
string :usage #用途
string :desc #描述
string :file, array: true
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}

```


## 带队人员的员工列表
### 链接: GET   /employees/recruiter_user_employees
#### 参数
```
requires! :recruiter_user_id
optional! :gender
optional! :state
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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


## 社保变更列表
### 链接: GET   /insurances/should_be_changed_employee
#### 参数
```
optional! :company_id
optional! :contract_id
optional! :recruiter_user_id
optional! :contract_state
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


## 企业工资表的人员列表
### 链接: GET   /payrolls/:id
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



## 企业工资表导出
### 链接: GET   /payrolls/export_excel
#### 参数
```
payroll_id
```
#### 返回值
```

```


## 企业工资表导入
### 链接: POST   /payrolls/import_excel
#### 参数
```
payroll_id
file
```
#### 返回值
```
{
    "code": 0,
    "message": "ok"
}
```



## todo-员工
### 链接: GET   /todos/employees
#### 参数
```
```
#### 返回值
```
{
    "code": 0, 
    "new_employees": [],
    "update_employees": [],
    "destroy_employees": [],
    "employee_renew_contracts": [],
    "employee_interior_circulations": [],
    "employee_leave_offices": []
}
```

## todo-保险
### 链接: GET   /todos/insurances
#### 参数
```
```
#### 返回值
```
{
    "code": 0, 
    "employee_buy_insurances": [],
    "employee_stop_insurances": []
}
```


## todo-薪资
### 链接: GET   /todos/payrolls
#### 参数
```
```
#### 返回值
```
{
    暂未写到
}
```


## todo-单位
### 链接: GET   /todos/payrolls
#### 参数
```
```
#### 返回值
```
{
    "code": 0, 
    "new_organizations": [],
    "update_organizations": [],
    "destroy_organizations": [],
    "new_agreements": [],
    "update_agreements": [],
    "destroy_agreements": [],
    "new_recruitment_projects": [],
    "update_recruitment_projects": [],
    "destroy_recruitment_projects": []
}
```


## 删除单位协议
### 链接: DELETE   /agreement/:id
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



## 删除员工
### 链接: DELETE   /employees/:id
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


## 删除单位
### 链接: DELETE   /organizations/:id
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


## 删除单位招聘项目
### 链接: DELETE   /recruitment_projects/:id
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

