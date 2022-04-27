# import os
# import m2
# m2.printSelf()
# from swl.aa import printSelf
# printSelf()
# from swl import aa
# aa.printSelf()
# aa.swl_swl()
from basic.数据库 import mysql_read
import requests
sql="select id from fanwe_user where user_name='billionmire'"
sql_name ="select user_name from fanwe_user where id=306"
name=(mysql_read(sql_name)[0][0])
login_data={
    "email":name,
    "user_pwd":"dHBxcExJWVBnWk1HSXhxRmJ4SVhETG9SZEdUWWluWnZnRGJwSldWaU9BeHNhVGlDVUglMjV1NjVCOSUyNXU3RUY0cXExMjM0JTI1dThGNkYlMjV1NEVGNg==",
    "ajax":"1",
}
login_url="http://106.52.182.140/fanwe/index.php?ctl=user&act=dologin&fhash=buMWlHgLwABpFowpyBUdVzrdsqXDytIHvkBPeuNVYZwxactean"
login_header={"Cookie":"ECS[visit_times]=1; PHPSESSID=jtp309qe0srmge3jmgllq9d884"}
login_result=requests.post(url=login_url,data=login_data,headers=login_header)
print(login_result.text)d


