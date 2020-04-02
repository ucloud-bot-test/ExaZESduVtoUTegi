# 攻击发生次数概览-StatWafAttacksTrend

UEWAF攻击发生次数概览

# Request Parameters
|Parameter name|Type|Description|Required|
|---|---|---|---|
|ProjectId|string|项目ID，不填表示默认项目|No|
|BeginTime|int|开始时间，时间戳表示,单位：秒|**Yes**|
|EndTime|int|结束时间，时间戳表示，单位：秒|**Yes**|
|Domain|string|要统计的域名|**Yes**|
|Extent|string|统计区间，单位：秒，取值范围0-7200|No|

# Response Elements
|Parameter name|Type|Description|Required|
|---|---|---|---|
|RetCode|int|返回码|**Yes**|
|Action|string|操作名称|**Yes**|
|Result|object|攻击详情，参考StatAttackResult|No|

## StatAttackResult
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Count|int|返回节点个数|**Yes**|
|Detail|array|攻击次数详情数组，参考StatAttackDetail|**Yes**|

## StatAttackDetail
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Timestamp|int|时间戳|**Yes**|
|Count|string|攻击次数|**Yes**|

# Request Example
```
https://api.ucloud.cn/?Action=StatWafAttacksTrend
&BeginTime=9
&EndTime=3
&Domain=YZxvwIed
&Extent=RQbnLjry
```

# Response Example
```
{
    "Action": "StatWafAttacksTrendResponse", 
    "RetCode": 0, 
    "Detail": [
        {
            "Count": "sTZCxiBq", 
            "Timestamp": 4
        }
    ]
}
```
