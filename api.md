# 地图api接口

## 腾讯地图

```
https://apis.map.qq.com/ws/geocoder/v1/?
location=39.984154,116.307490
&get_poi=0
&key=ET7BZ-TDHL6-SCKSH-MAIJR-YKTIE-7LFCO
```

返回结果：
```json
{
    "status":0,
    "message":"query ok",
    "request_id":"8e46c92c-457c-11ea-96bb-525400180013",
    "result":{
        "location":{
            "lat":39.984154,
            "lng":116.30749
        },
        "address":"北京市海淀区北四环西路66号",
        "formatted_addresses":{
            "recommend":"海淀区中关村中国技术交易大厦(彩和坊路)",
            "rough":"海淀区中关村中国技术交易大厦(彩和坊路)"
        },
        "address_component":{
            "nation":"中国",
            "province":"北京市",
            "city":"北京市",
            "district":"海淀区",
            "street":"北四环西路",
            "street_number":"北四环西路66号"
        }
    }
}
```

## 高德地图

请求接口：
```
https://restapi.amap.com/v3/geocode/regeo?
output=JSON
&location=116.310003,39.991957
&key=<用户的key>
&radius=0
&extensions=base
&batch=false
&roadlevel=0
```

返回结果：
```json
{
    "status" :"1",
    "regeocode" :{
        "addressComponent" :{
            "city" :[ ],
            "province" :"北京市",
            "adcode" :"110105",
            "district" :"朝阳区",
            "towncode" :"110105026000",
            "streetNumber" :{ … },
            "country" :"中国",
            "township" :"望京街道",
            "businessAreas" :[ … ],
            "building" :{ … },
            "neighborhood" :{ … },
            "citycode" :"010"
        },
        "formatted_address" :"北京市朝阳区望京街道方恒国际中心B座方恒国际中心"
    },
    "info" :"OK",
    "infocode" :"10000"
}
```

## 百度地图

```
http://api.map.baidu.com/reverse_geocoding/v3/?
ak=40NVD4ntV7xVqDdMifmygyxm0O1B1MM7
&output=json
&coordtype=wgs84ll
&location=31.225696563611,121.49884033194
```

结果：
```json
{
    "status": 0,
    "result": {
        "location": {
            "lng": 121.50989077799084,
            "lat": 31.22932842411674
            },
        "formatted_address": "上海市黄浦区中山南路187",
        "business": "外滩,陆家嘴,董家渡",
        "addressComponent": {
            "country": "中国",
            "country_code": 0,
            "country_code_iso": "CHN",
            "country_code_iso2": "CN",
            "province": "上海市",
            "city": "上海市",
        }
    }
}
```
