# 公共接口

## 图片上传
/upload/imgupload

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 | 
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| file | 图片文件 | File | true | |  

返回格式‘’‘’

```json
{
  "code": 1,
  "msg": "",
  "dataSingle": {
    //图片返回路径
    "image_full_path"：图片访问全路径，包括http://
    "image_path"：	//图片上传相对路径，用于保存到数据库中
    "image_name"：	//图片名称，包括后缀名
},
  "dataArray": null
}
```

#### JSONDATA
```jsondata
{
  "code": 0,
  "msg": "",
  "dataSingle": {
    "image_full_path"："http://img.junjieboche.cn/img/upload/123123213.jpg"
    "image_path"："/img/upload/123123213.jpg"
    "image_name"："123123213.jpg"
  },
  "dataArray": ""
}
```