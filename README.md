### 软件工程项目


### API文档

#### 0x00 登录接口

* url:http://iot.wduozhi.xyz/api/user/login
* method:post

##### get

* username
* password

##### return

```
{
    "data": {
        "id": 1,
        "username": "coding",
        "nick_name": "小智e",
        "status": 1
    },
    "message": null,
    "status": "success"
}

{
    "data": null,
    "message": "passwrd error or user not exist",
    "status": "error"
}
```


#### 0x01 添加网关

* url:http://iot.wduozhi.xyz/api/gateway
* method:post

##### get

* ip
    - ip,string
* port
    - 端口,string
* description
    - 描述,string
* location
    - 地点，位置,string

##### return

```
{
    "data": {
        "id": 7,
        "ip": "127.0.0.1",
        "port": "8080",
        "description": "haha，我是网关6号",
        "location": "天马-1-3-135",
        "status": 1
    },
    "message": null,
    "status": "success"
}
```

#### 0x02 获取全部网关信息

* url:http://iot.wduozhi.xyz/api/gateway
* method:get

##### get

null

##### return

```
{
    "data": [
        {
            "id": 2,
            "ip": "127.0.0.1",
            "port": "8080",
            "description": "haha，我是网关1号",
            "location": "天马-1-3-135",
            "status": 1
        },
        {
            "id": 3,
            "ip": "127.0.0.1",
            "port": "8080",
            "description": "haha，我是网关2号",
            "location": "天马-1-3-135",
            "status": 1
        }
    ],
    "message": null,
    "status": "success"
}
```

#### 0x03 根据id获取网关信息

* url:http://iot.wduozhi.xyz/api/gateway/{1d}
* method:get

##### get

* id

##### return
```
{
    "data": {
        "id": 2,
        "ip": "127.0.0.1",
        "port": "8080",
        "description": "haha，我是网关1号",
        "location": "天马-1-3-135",
        "status": 1
    },
    "message": "",
    "status": "success"
}
```

#### 0x03-1 修改网关信息

* url:http://iot.wduozhi.xyz/api/gateway
* method:put

##### get
* id
    - 网关id
* ip
    - ip,string
* port
    - 端口,string
* description
    - 描述,string
* location
    - 地点，位置,string


##### return 

```
{
    "data": {
        "id": 1,
        "ip": "127.0.0.1",
        "port": "8080",
        "description": "网关1号",
        "location": "天马-1-3-135",
        "status": 0
    },
    "message": null,
    "status": "success"
}
```

#### 0x03-2 删除网关

* url:http://iot.wduozhi.xyz/api/gateway/{1d}
* method:delete

##### get

* id

##### return
```
{
    "data": null,
    "message": null,
    "status": "success"
}
```



#### 0x04 添加传感器

* url:http://iot.wduozhi.xyz/api/sensor
* method:post

##### get

* description
    - 描述,string
* location
    - 地点,string
* factory
    - 厂商,string
* install_time
    - 安装时间,时间戳
* maintenance_time
    - 维修截止时间,时间戳
* produce_date:1234567890000
    - 生产时间,时间戳
* gate_id
    - 传感器id
* classify_id
    - 传感器类型id


##### return 

```
{
    "data": {
        "id": 6,
        "description": "haha，我是网关四号",
        "location": "天马-1-3-135",
        "factory": "华美集团",
        "install_time": "2009-02-13T23:31:30.000+0000",
        "produce_date": "2009-02-13T23:31:30.000+0000",
        "maintenance_time": "2009-02-13T23:31:30.000+0000",
        "status": 1
    },
    "message": "",
    "status": "success"
}
```

#### 0x04-1 修改传感器

* url:http://iot.wduozhi.xyz/api/sensor
* method:put

##### get
* id
    - 传感器id
* description
    - 描述,string
* location
    - 地点,string
* factory
    - 厂商,string
* install_time
    - 安装时间,时间戳
* maintenance_time
    - 维修截止时间,时间戳
* produce_date:1234567890000
    - 生产时间,时间戳
* gate_id
    - 传感器id
* classify_id
    - 传感器类型id


##### return 

```
{
    "data": {
        "id": 6,
        "description": "haha，我是网关四号",
        "location": "天马-1-3-135",
        "factory": "华美集团",
        "install_time": "2009-02-13T23:31:30.000+0000",
        "produce_date": "2009-02-13T23:31:30.000+0000",
        "maintenance_time": "2009-02-13T23:31:30.000+0000",
        "status": 1
    },
    "message": "",
    "status": "success"
}
```



#### 0x05 根据id获取传感器信息

* url:* url:http://iot.wduozhi.xyz/api/sensor/{id}
* method:get

##### get

* id

##### return

```
{
    "data": {
        "id": 3,
        "description": "haha，我是网关一号",
        "location": "天马-1-3-135",
        "factory": "华美集团",
        "install_time": "2009-02-13T23:31:30.000+0000",
        "produce_date": "2009-02-13T23:31:30.000+0000",
        "maintenance_time": "2009-02-13T23:31:30.000+0000",
        "status": 1
    },
    "message": "",
    "status": "success"
}
```

#### 0x05-1 根据id删除传感器

* url:* url:http://iot.wduozhi.xyz/api/sensor/{id}
* method:delete

##### get

id

##### return

```
{
    "data": null,
    "message": "",
    "status": "success"
}
```



#### 0x06 获取某网关下的传感器列表

* url:* url:http://iot.wduozhi.xyz/api/gateway/sensors/{id}
* method:get

##### get

* gateway's id

##### return
```
{
    "data": [
        {
            "id": 2,
            "description": "haha，我是一个小小的网关",
            "location": "天马-1-3-135",
            "factory": "华美集团",
            "install_time": "2009-02-13T23:31:30.000+0000",
            "produce_date": "2009-02-13T23:31:30.000+0000",
            "maintenance_time": "2009-02-13T23:31:30.000+0000",
            "status": 1
        },
        {
            "id": 3,
            "description": "haha，我是网关一号",
            "location": "天马-1-3-135",
            "factory": "华美集团",
            "install_time": "2009-02-13T23:31:30.000+0000",
            "produce_date": "2009-02-13T23:31:30.000+0000",
            "maintenance_time": "2009-02-13T23:31:30.000+0000",
            "status": 1
        }
    ],
    "message": "",
    "status": "success"
}
```

#### 0x07 获取某网关下的传感器类型列表 


* url:http://iot.wduozhi.xyz/api/gateway/classify/{id} 
* method:get 

##### get

gateway's id

##### reurn 

```
{
    "data": [
        {
            "id": 1,
            "name": "温度传感器",
            "status": 1,
            "sensors": [
                {
                    "id": 3,
                    "description": "haha，我是网关一号",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-13T23:31:30.000+0000",
                    "produce_date": "2009-02-13T23:31:30.000+0000",
                    "maintenance_time": "2009-02-13T23:31:30.000+0000",
                    "status": 1
                },
                {
                    "id": 6,
                    "description": "haha，我是网关四号",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-13T23:31:30.000+0000",
                    "produce_date": "2009-02-13T23:31:30.000+0000",
                    "maintenance_time": "2009-02-13T23:31:30.000+0000",
                    "status": 1
                }
            ]
        },
        {
            "id": 2,
            "name": "湿度传感器_1",
            "status": 1,
            "sensors": [
                {
                    "id": 4,
                    "description": "haha，我是网关二号",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-13T23:31:30.000+0000",
                    "produce_date": "2009-02-13T23:31:30.000+0000",
                    "maintenance_time": "2009-02-13T23:31:30.000+0000",
                    "status": 1
                }
            ]
        },
        {
            "id": 3,
            "name": " 湿度传感器_2",
            "status": 1,
            "sensors": [
                {
                    "id": 5,
                    "description": "haha，我是网关三号",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-13T23:31:30.000+0000",
                    "produce_date": "2009-02-13T23:31:30.000+0000",
                    "maintenance_time": "2009-02-13T23:31:30.000+0000",
                    "status": 1
                }
            ]
        }
    ],
    "message": "",
    "status": "success"
}
```

#### 0x08 添加传感器类型

* url:http://iot.wduozhi.xyz/api/classify 
* method:post

##### get

* name
    - 类型名称，string

##### return 

```
{
    "data": {
        "id": 4,
        "name": "湿度传感器",
        "status": 1,
        "sensors": null
    },
    "message": "",
    "status": "success"
}
```

#### 0x09 获取所有传感器类型

* url:http://iot.wduozhi.xyz/api/classify
* method:get

##### get 

null

##### return 

```
{
    "data": [
        {
            "id": 1,
            "name": "温度传感器",
            "status": 1,
            "sensors": null
        },
        {
            "id": 2,
            "name": "湿度传感器_1",
            "status": 1,
            "sensors": null
        },
        {
            "id": 3,
            "name": " 湿度传感器_2",
            "status": 1,
            "sensors": null
        },
        {
            "id": 4,
            "name": "湿度传感器_3",
            "status": 1,
            "sensors": null
        }
    ],
    "message": "",
    "status": "success"
}
```

#### 0xA 获取某传感器类型下的传感器

* url：http://iot.wduozhi.xyz/api/classify/sensors/{id}
* method:get

##### get

classify's id

##### return

```
{
    "data": [
        {
            "id": 3,
            "description": "haha，我是网关一号",
            "location": "天马-1-3-135",
            "factory": "华美集团",
            "install_time": "2009-02-13T23:31:30.000+0000",
            "produce_date": "2009-02-13T23:31:30.000+0000",
            "maintenance_time": "2009-02-13T23:31:30.000+0000",
            "status": 1
        },
        {
            "id": 6,
            "description": "haha，我是网关四号",
            "location": "天马-1-3-135",
            "factory": "华美集团",
            "install_time": "2009-02-13T23:31:30.000+0000",
            "produce_date": "2009-02-13T23:31:30.000+0000",
            "maintenance_time": "2009-02-13T23:31:30.000+0000",
            "status": 1
        }
    ],
    "message": "",
    "status": "success"
}
```

#### 0xB 下载网关信息

* url：http://iot.wduozhi.xyz/api/file/gatway?id=1
* method:get

##### get

* id

##### return

file


#### 0xC 下载传感器信息

* url：http://iot.wduozhi.xyz/api/file/sensor?id=1
* method:get

##### get

* id

##### return

file


#### 0xD 根据传感器id获取其数据

* url：http://iot.wduozhi.xyz/api/sensor/data/{id}
* method:get

##### get

* id

##### return

```aidl{
    "data": [
        {
            "id": 1,
            "data": 0.530177,
            "time": "1970-01-02 10:17:36",
            "status": 1
        },
        {
            "id": 2,
            "data": 0.657997,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 3,
            "data": 0.733731,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 4,
            "data": 0.848276,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 5,
            "data": 0.271506,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 6,
            "data": 0.930852,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 7,
            "data": 0.456563,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 8,
            "data": 0.00616956,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 9,
            "data": 0.754887,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 10,
            "data": 0.411689,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 11,
            "data": 0.470635,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 12,
            "data": 0.743208,
            "time": "2018-11-27 02:08:03",
            "status": 1
        },
        {
            "id": 13,
            "data": 0.00801748,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 14,
            "data": 0.269272,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 15,
            "data": 0.935274,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 16,
            "data": 0.540042,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 17,
            "data": 0.766006,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 18,
            "data": 0.445037,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 19,
            "data": 0.708111,
            "time": "2018-11-27 02:08:04",
            "status": 1
        },
        {
            "id": 20,
            "data": 0.29987,
            "time": "2018-11-27 02:08:05",
            "status": 1
        },
        {
            "id": 21,
            "data": 0.415965,
            "time": "2018-11-27 02:08:05",
            "status": 1
        },
        {
            "id": 22,
            "data": 0.00319862,
            "time": "2018-11-27 02:08:05",
            "status": 1
        },
        {
            "id": 23,
            "data": 0.458684,
            "time": "2018-11-27 02:08:05",
            "status": 1
        },
        {
            "id": 24,
            "data": 0.597285,
            "time": "2018-11-27 02:08:05",
            "status": 1
        },
        {
            "id": 25,
            "data": 0.53315,
            "time": "2018-11-27 02:08:06",
            "status": 1
        },
        {
            "id": 26,
            "data": 0.248055,
            "time": "2018-11-27 02:08:06",
            "status": 1
        },
        {
            "id": 27,
            "data": 0.302649,
            "time": "2018-11-27 02:08:06",
            "status": 1
        },
        {
            "id": 28,
            "data": 0.340144,
            "time": "2018-11-27 02:08:06",
            "status": 1
        },
        {
            "id": 29,
            "data": 0.791612,
            "time": "2018-11-27 02:08:07",
            "status": 1
        },
        {
            "id": 30,
            "data": 0.153431,
            "time": "2018-11-27 02:08:07",
            "status": 1
        },
        {
            "id": 31,
            "data": 0.242326,
            "time": "2018-11-27 02:08:07",
            "status": 1
        }
    ],
    "message": "",
    "status": "success"
}
```


#### 0xE 修改密码

* url：http://iot.wduozhi.xyz/api/user/password
* method:post

##### get

* id
* oldPassword
* newPassword


##### return

{
    
}


#### 0xF 修改个人信息

* url：http://iot.wduozhi.xyz/api/user/modify
* method:post

##### get

* id
* newUsername
* newTel
* newEmail


##### return

{
    
}


#### 0x10 获取所有传感器异常

* url:http://iot.wduozhi.xyz/api/sensorException
* method:get

##### get 

null

##### return 

```
{
    "data": [
        {
            "id": 1,
            "description": "haha，我没电了",
            "time": "2018-12-13",
            "status": 0,
            "gateway": {
                "id": 2,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "haha，我是网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        },
        {
            "id": 2,
            "description": "haha，我断电了",
            "time": "2018-12-20",
            "status": 0,
            "gateway": {
                "id": 1,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        }
    ],
    "message": null,
    "status": "success"
}
```



#### 0x11 获取所有网关异常

* url:http://iot.wduozhi.xyz/api/gatewayException
* method:get

##### get 

null

##### return 

```
{
    "data": [
        {
            "id": 1,
            "description": "haha，我没电了",
            "time": "2018-12-13",
            "status": 0,
            "gateway": {
                "id": 2,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "haha，我是网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        },
        {
            "id": 2,
            "description": "haha，我断电了",
            "time": "2018-12-20",
            "status": 0,
            "gateway": {
                "id": 1,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        }
    ],
    "message": null,
    "status": "success"
}
```

#### 0x12 获取一段时间内传感器异常

* url:http://iot.wduozhi.xyz/api/sensorException/{timetamp}
* method:get
* 注解：timetamp 为 {dateFromtamp@dateToTamp} 示例 {1514773035@1545360731}为起始时间的unix时间戳和终止时间的unix时间戳

##### get 

* dataFrom
* dataTo

##### return 

```
{
    "data": [
        {
            "id": 1,
            "description": "haha，我没电了",
            "time": "2018-12-13",
            "status": 0,
            "gateway": {
                "id": 2,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "haha，我是网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        },
        {
            "id": 2,
            "description": "haha，我断电了",
            "time": "2018-12-20",
            "status": 0,
            "gateway": {
                "id": 1,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        }
    ],
    "message": null,
    "status": "success"
}
```


#### 0x13 获取一段时间内网关异常

* url:http://iot.wduozhi.xyz/api/gatewayException/{timetamp}
* method:get
* 注解：timetamp 为 {dateFromtamp@dateToTamp} 示例 {1514773035@1545360731} 为起始时间的unix时间戳和终止时间的unix时间戳

##### get 

* dataFrom,dataTo

##### return 

```
{
    "data": [
        {
            "id": 1,
            "description": "haha，我没电了",
            "time": "2018-12-13",
            "status": 0,
            "gateway": {
                "id": 2,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "haha，我是网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        },
        {
            "id": 2,
            "description": "haha，我断电了",
            "time": "2018-12-20",
            "status": 0,
            "gateway": {
                "id": 1,
                "ip": "127.0.0.1",
                "port": "8080",
                "description": "网关1号",
                "location": "天马-1-3-135",
                "status": 1
            }
        }
    ],
    "message": null,
    "status": "success"
}
```


#### 0x14 获取所有传感器异常(分页版本)

* url:http://iot.wduozhi.xyz/api/sensorException/page/{page}
* method:get

##### get 

* page

##### return 

```
{
    "data": {
        "content": [
            {
                "id": 81,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 4,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关3号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 80,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 3,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关2号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 79,
                "description": "连接异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 4,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关3号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 78,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 3,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关2号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 77,
                "description": "未接收到数据",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 1,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "网关1号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 76,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 3,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关2号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 75,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 1,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "网关1号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 74,
                "description": "数据异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 1,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "网关1号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 73,
                "description": "连接异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 4,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关3号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            },
            {
                "id": 72,
                "description": "数据异常",
                "time": "2018-12-27",
                "status": 1,
                "gateway": {
                    "id": 3,
                    "ip": "127.0.0.1",
                    "port": "8080",
                    "description": "haha，我是网关2号",
                    "location": "天马-1-3-135",
                    "status": 1
                }
            }
        ],
        "pageable": {
            "sort": {
                "sorted": true,
                "unsorted": false
            },
            "offset": 0,
            "pageSize": 10,
            "pageNumber": 0,
            "paged": true,
            "unpaged": false
        },
        "totalElements": 81,
        "totalPages": 9,
        "last": false,
        "number": 0,
        "size": 10,
        "sort": {
            "sorted": true,
            "unsorted": false
        },
        "numberOfElements": 10,
        "first": true
    },
    "message": null,
    "status": "success"
}
```



#### 0x15 获取所有网关异常(分页版本)

* url:http://iot.wduozhi.xyz/api/gatewayException/page/{page}
* method:get

##### get 

* page

##### return 

```
{
    "data": {
        "content": [
            {
                "id": 15819,
                "description": "未接收到数据",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 7,
                    "description": "检测温度",
                    "location": "机房2",
                    "factory": "中国",
                    "install_time": "2018-11-17",
                    "produce_date": "1970-01-23",
                    "maintenance_time": "1970-01-23",
                    "status": 1,
                    "sensorClassify": {
                        "id": 1,
                        "name": "温度传感器",
                        "status": 1
                    }
                }
            },
            {
                "id": 15818,
                "description": "连接异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 3,
                    "description": "我是网关一号233",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-09",
                    "produce_date": "2009-02-09",
                    "maintenance_time": "2009-02-09",
                    "status": 1,
                    "sensorClassify": {
                        "id": 1,
                        "name": "温度传感器",
                        "status": 1
                    }
                }
            },
            {
                "id": 15817,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 20,
                    "description": "new",
                    "location": "434",
                    "factory": "信息科学与工程学院",
                    "install_time": "2018-12-02",
                    "produce_date": "2018-11-30",
                    "maintenance_time": "2018-12-21",
                    "status": 1,
                    "sensorClassify": {
                        "id": 3,
                        "name": " 湿度传感器_2",
                        "status": 1
                    }
                }
            },
            {
                "id": 15816,
                "description": "网络异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 10,
                    "description": "检测机房二号服务器",
                    "location": "天马135",
                    "factory": "哈哈",
                    "install_time": "2018-11-17",
                    "produce_date": "2018-10-30",
                    "maintenance_time": "2018-11-28",
                    "status": 1,
                    "sensorClassify": {
                        "id": 2,
                        "name": "湿度传感器_1",
                        "status": 1
                    }
                }
            },
            {
                "id": 15814,
                "description": "连接异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 16,
                    "description": "哈哈哈哈",
                    "location": "哈哈",
                    "factory": "哈哈",
                    "install_time": "2018-11-18",
                    "produce_date": "2018-10-31",
                    "maintenance_time": "2018-11-29",
                    "status": 1,
                    "sensorClassify": {
                        "id": 1,
                        "name": "温度传感器",
                        "status": 1
                    }
                }
            },
            {
                "id": 15813,
                "description": "未接收到数据",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 11,
                    "description": "哈哈哈哈",
                    "location": "哈哈",
                    "factory": "哈哈",
                    "install_time": "2018-11-18",
                    "produce_date": "2018-10-31",
                    "maintenance_time": "2018-11-29",
                    "status": 1,
                    "sensorClassify": {
                        "id": 1,
                        "name": "温度传感器",
                        "status": 1
                    }
                }
            },
            {
                "id": 15815,
                "description": "数据异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 8,
                    "description": "检测湿度",
                    "location": "机房3",
                    "factory": "中国",
                    "install_time": "2018-11-17",
                    "produce_date": "2018-10-30",
                    "maintenance_time": "2018-11-28",
                    "status": 1,
                    "sensorClassify": {
                        "id": 2,
                        "name": "湿度传感器_1",
                        "status": 1
                    }
                }
            },
            {
                "id": 15812,
                "description": "数据异常",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 9,
                    "description": "检测湿度",
                    "location": "主站",
                    "factory": "中国",
                    "install_time": "2018-11-18",
                    "produce_date": "2018-10-31",
                    "maintenance_time": "2018-11-29",
                    "status": 1,
                    "sensorClassify": {
                        "id": 2,
                        "name": "湿度传感器_1",
                        "status": 1
                    }
                }
            },
            {
                "id": 15810,
                "description": "未接受到数据",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 4,
                    "description": "我是传感器4号",
                    "location": "天马-1-3-135",
                    "factory": "中国制造",
                    "install_time": "2009-02-07",
                    "produce_date": "2009-02-07",
                    "maintenance_time": "2009-02-07",
                    "status": 1,
                    "sensorClassify": {
                        "id": 2,
                        "name": "湿度传感器_1",
                        "status": 1
                    }
                }
            },
            {
                "id": 15811,
                "description": "未接受到数据",
                "time": "2018-12-27",
                "status": 1,
                "sensor": {
                    "id": 3,
                    "description": "我是网关一号233",
                    "location": "天马-1-3-135",
                    "factory": "华美集团",
                    "install_time": "2009-02-09",
                    "produce_date": "2009-02-09",
                    "maintenance_time": "2009-02-09",
                    "status": 1,
                    "sensorClassify": {
                        "id": 1,
                        "name": "温度传感器",
                        "status": 1
                    }
                }
            }
        ],
        "pageable": {
            "sort": {
                "sorted": true,
                "unsorted": false
            },
            "offset": 20,
            "pageSize": 10,
            "pageNumber": 2,
            "unpaged": false,
            "paged": true
        },
        "last": false,
        "totalElements": 401,
        "totalPages": 41,
        "number": 2,
        "size": 10,
        "numberOfElements": 10,
        "sort": {
            "sorted": true,
            "unsorted": false
        },
        "first": false
    },
    "message": null,
    "status": "success"
}
```


#### 0x16 下载全部的网关异常

* url:http://iot.wduozhi.xyz/api/download/GatewayException
* method:get

##### get 

null

##### return 

```
GatewayExceptions.xls

```


#### 0x17 下载全部的传感器异常

* url:http://iot.wduozhi.xyz/api/download/SensorException
* method:get

##### get 

null

##### return 

```
SensorExceptions.xls

```

