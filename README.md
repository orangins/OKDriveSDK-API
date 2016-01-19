# OKDriveSDK-API
## OKDrive工作流程
![OKDriveSDK序列图](http://7i7itm.com1.z0.glb.clouddn.com/OKDrive-UML-%E6%B5%81%E7%A8%8B.png)
## 行程通知接口（Trip Nofity）
### 接口地址
接口地址由合作方提供，在用户行程上传到OKDrive并且OKDrive处理完成之后，会回调合作方提供的接口。
### 参数
OKDrive调用此接口时附带如下参数，目前仅支持json格式
{"version":1,"type":"TRIP_NOTIFY_V3","driver_id":"{DRIVER_ID}","trip_id":{TRIP_ID}}

例如：
{"version":1,"type":"TRIP_NOTIFY_V3","driver_id":"driver_1000","trip_id":1452321900111}

__合作方服务器接收到此接口回调之后，保存driver_id和trip_id，并返回"success"，否则OKDrive服务器会认为合作方保存失败，会持续定时重新发起回调__

## 用户信息接口（Driver Info)
发送邮件到okdrive#okchexian.com（请将#替换成@）获取测试接口地址
## 行程信息接口 (Trip Info)
发送邮件到okdrive#okchexian.com（请将#替换成@）获取测试接口地址