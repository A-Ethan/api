# 获取主机业务组列表-DescribeUHostTags

获取指定数据中心的业务组列表。

# Request Parameters
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Region|string|地域。 参见 [地域和可用区列表](api/summary/regionlist)|**Yes**|
|Zone|string|可用区。参见 [可用区列表](api/summary/regionlist)|No|
|ProjectId|string|项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](api/summary/get_project_list)|No|

# Response Elements
|Parameter name|Type|Description|Required|
|---|---|---|---|
|RetCode|int|返回码|**Yes**|
|Action|string|操作名称|**Yes**|
|TotalCount|int|已有主机的业务组总数|No|
|TagSet|array|业务组集合见 UHostTagSet|No|

## UHostTagSet
|Parameter name|Type|Description|Required|
|---|---|---|---|
|Tag|string|业务组名称|No|
|TotalCount|int|该业务组中包含的主机个数|No|
|Zone|string|可用区|No|

# Request Example
```
https://api.ucloud.cn/?Action=DescribeUHostTags
&Region=cn-bj2
&Zone=cn-bj2-04
&ProjectId=org-xxx
```

# Response Example
```
{
    "Action": "DescribeUHostTagsResponse", 
    "TotalCount": 1, 
    "RetCode": 0, 
    "TagSet": [
        {
            "TotalCount": 2, 
            "Tag": "Default", 
            "Zone": "xxx"
        }
    ]
}
```

