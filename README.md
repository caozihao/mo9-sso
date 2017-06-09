# mo9-sso

适用场合：<br>
当后台是node作为服务的时候

用途：<br>
判断权限和获取用户状态等业务逻辑的模块


使用方法:<br><br>
**request**
``` javascript
    url:远程获取ticket信息的请求地址
    userInfo:存储在session中的userInfo对象
```

**response**
``` javascript
  {
        "code" : {
            "type" : "integer",
            "description" : "报错号,0表示没有错误，1041表示登录失效"
        },
        "data" : {
            "description" : "session对象"
            "type" : "object",
            "properties":{
                "userInfo":{
                    "description" : "用户信息",
                    "type" : "object"
                 }
            }
        }
        "message" : {
            "type" : "string",
            "description" : "错误信息,如果未出错,则此字段没值"
        }
   }
```




