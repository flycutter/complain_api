
### 投诉单推送接口:

接口地址：   
```
http://ecomplain.12301.cn/api/complaint_order/push
```
请求方式：   
```
post
```
数据格式：   
```
json
```
example:   
```
    "address_ts":"重庆市江北区建新北路38号世纪英皇北塔24楼",
    "verification_code":"cdjhfkr4590skalmch",
    "sex":"2",
    "unitname":"游客",
    "date_am":"2017-01-13 00:00:00",
    "tel":"15111834504",
    "order_sort":"3",
    "way":"1",
    "date_ts":"2017-01-16",
    "travel_sort":"3",
    "order_no":"2017011610386",
    "city":"1029007000",
    "tel_ts":"023-88611111",
    "zip_ts":null,
    "times":"0",
    "facts":"诉求方：胡杰（联系方式：11111111111，证件编号：111111111111111111）其余1人信息已告知收集；\r\n被诉方：重庆渝之旅国际旅行社有限公司（联系方式:023-88111111）；\r\n投诉事由：胡女士一行2人在重庆渝之旅国际旅行社有限公司报名参加泰国清迈游，行程日期：1月7日-1月12日，团费：共2358元。胡女士表示：1、行程第二天，地接导游擅自甩团；2、地接导游随意变更行程，实际行程与行程单完全不符，地接导游利用言语诱惑其花费400元参加自费项目清莱1日游，花费200元参观泰国人妖表演；3、行程前几天，其一直是坐在大巴车前面的座位，行程最后一天，地接导游让其坐在最后面的座位，因最后面的座位比较脏乱，其跟导游协商能否坐到之前的座位，地接导游服务态度非常恶劣，胡女士表示因前一天晚上参加自费项目，其一行人向领队反馈，后领队表示要求地接导游给游客道歉，导致地接导游故意针对其，对其进行殴打，后通过其他游客的协助下，地接导游不情愿的给其道歉。回程后，针对以上问题，找旅行社索要大巴车的监控，旅行社未给其提供，针对导游殴打游客的问题，旅行社只给其赔偿500元/人，双方协商未果，胡女士对此不满，故投诉（有合同、行程单，无发票）。",
    "request":"投诉重庆渝之旅国际旅行社有限公司导游服务质量问题，要求旅行社赔偿共2400元。",
    "name":"胡杰",
    "code_num":"111111111111111111",
    "updater":"重庆市,南岸区",
    "sort_ts_main":"3",
    "code_sort":"1",
    "channel_type":"12301[热线]",
    "destination":"1029007000",
    "unit_sort":"1",
    "unitname_ts":"重庆渝之旅国际旅行社有限公司(L-CQ-CJ00014)",
    "nationality":"中国",
    "happened":"1029007000",
    "source":"500108",
    "address":"",
    "sub_sort_ts_main":null,
    "accept_num":"2",
    "ts_unitid":"a_aaaaaaaaa",
    "fujian_urls":"http://www.cy12301.com/csr/attach/downFile?filePathName=../files/1484561011405.rar",
    "ts_obj_main_new": "1",       //一级分类
    "ts_obj_sec_new": "1",          //二级分类
    "ts_obj_child_new": "3"，
    "flows":[{create_time:'2017-07-15 12:12:12',order_no:'12301',operator:'12301客服',action:'上传投诉单',state:'待受理',note:'上传',apartment:'12301客服'}],
    "expire_time": "2017.06.01 12:30:00"
```
说明：该接口可用作创建和更新；此数据结构是完全参照投诉平台的，仅增加一个字段expire_time，用来标明该投诉单的企业操作过期时间

### 投诉单锁定接口

接口地址：
```
http://ecomplain.12301.cn/api/complaint_order/lock
```
请求方式：   
```
post
```
数据格式：   
```
json
```
example:   
```
order_no: '2017011610386'
```
说明：当质监人员点击上传按钮后，CSR调用该接口，智旅通企业版会将该投诉单锁定

### 调用接口的返回值：

```
'0000':调用接口成功
'1002':数据库操作失败
'1003':工单号为空
```

