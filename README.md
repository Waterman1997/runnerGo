

RunnerGo is a develop tool similar to apache bench (ab).

## Usage
RunnerGo is designed to be the simplest way possible to make stress test. 

```
1. Install go. See https://golang.google.cn/dl/
2. go build runnerGo.go
3. ./runnerGo
```

```
Options:
    -p 	server port     
    -a 	is auto exit
```
## Request Para

```javascript
{
    "c": 2,
    "n": 2,
    "target_id":"",
    "report_time":0,
    "log_type":0,
    "data": {
        "method": "POST",
        "url": "http://www.baidu.com",
        "mode": "urlencoded",
        "headers": [
            {
                "name": "Pragma",
                "value": "no-cache"
            },
            {
                "name": "Server",
                "value": "yisu.com"
            }
        ],
        "postData": {
            "text":"some data", // body for raw
            "params": [ // body for form-data/urlencoded
                {
                    "name": "logo",
                    "type": "file",
                    "value": "@/Users/root/Downloads/1.jpg"
                },
                {
                    "name": "title",
                    "value": "标题"
                }
            ]
        }
    }
}
```

## Examples
```json
{
    "code": 200,
    "message": "success",
    "data": {
        "Target_id":"xxx",
        "CompleteRequests": 4,
        "FailedRequests": 0,
        "SuccessRequests": 4,
        "TimeToken": 0.324641,
        "TotalDataSize": 2028,
        "AvgDataSize": 507,
        "RequestsPerSec": 12.32130260811173,
        "SuccessRequestsPerSec": 12.32130260811173,
        "MinUseTime": 60,
        "MaxUseTime": 249,
        "AvgUseTime": 156.25,
        "CodeDetail": {
            "200": 4
        },
        "WaitingTimeDetail": {
            "10.00%": 70,
            "25.00%": 70,
            "50.00%": 74,
            "75.00%": 232,
            "90.00%": 232,
            "95.00%": 232,
            "99.00%": 232,
            "99.90%": 232,
            "99.99%": 232
        },
        "AvgConn": 77.5,
        "MaxConn": 158,
        "MinConn": 0,
        "AvgDNS": 30.5,
        "MaxDNS": 61,
        "MinDNS": 0,
        "AvgReq": 0,
        "MaxReq": 0,
        "MinReq": 0,
        "AvgDelay": 77.5,
        "MaxDelay": 90,
        "MinDelay": 60,
        "AvgRes": 0,
        "MaxRes": 0,
        "MinRes": 0
    }
}
```

## demo
https://runnergo.apipost.cn/  
 ![示例图片](https://apipost.oss-cn-beijing.aliyuncs.com/cdn/runnergo/runnergo_demo.png) 

 本机需要先运行编译后的程序。可以在Releases中下载最新的编译好的程序

