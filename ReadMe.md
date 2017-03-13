
### nogizaka

#### 一、API部分

> 集成域名: `http://112.74.32.29:8081`

##### 1、分页获取新闻

- 接口地址:`/blogs/getBlogsByPage`
- 调用方式:`GET`
- 参数说明:

  参数名 | 类型 | 必填 | 备注
  --------- | -------------| --------- | -------------
  pageNo | int | 否 | 默认为0（表示第一页）
  pageSize | int | 否 | 默认为15
  desc | boolean | 否 | 默认为true（表示到倒排序）

- 返回

	```
	{
	  "content": [
	        {
            "id": 1,
            "name": "markdown测试",
            "summary": "summary",
            "content": "####%20%E6%95%88%E6%9E%9C%E5%9B%BE%EF%BC%9A%0A%0A!%5BhorizontalScrollView%5D(http://o7zh7nhn0.bkt.clouddn.com/horizontalScrollMoreLayout.gif)",
            "category": "cate",
            "created_time": 1486717321037,
            "image_url": "http://o7zh7nhn0.bkt.clouddn.com/auu88f43a5el3lk3gcajxajor.jpg"
          },
          ...
	  ],
	  "last": true,
	  "totalElements": 43,
	  "totalPages": 3,
	  "first": false,
	  "numberOfElements": 0,
	  "size": 15,
	  "number": 3
}
	```

##### 2、获取新闻详情

- 接口地址:`/blogs/getBlogDetailById`
- 调用方式:`GET`
- 参数说明:

  参数名 | 类型 | 必填 | 备注
  --------- | -------------| --------- | -------------
  id | int | 是 | 新闻id（主键）

- 返回

	```
	{
	  "responseData": {
	    "id": 5,
	    "name": "markdown测试",
	    "summary": "summary",
	    "content": "中文测试",
	    "category": "cate",
	    "created_time": 1486720729698,
	    "image_url": "http://o7zh7nhn0.bkt.clouddn.com/auu88f43a5el3lk3gcajxajor.jpg"
	  },
	  "code": 200,
	  "message": "success"
}
	```


##### 3、获取新闻种类

- 接口地址:`/blogs/getCategories`
- 调用方式:`GET`
- 返回

	```
	{
	  "responseData": [
	    "cate",
	    "h测试测试ahah",
	    ""
	  ],
	  "cde": 200,
	  "message": "success"
}
	```

##### 4、获取全部乃木坂的成员信息(包括三期)

- 接口地址:`/member/getAll`
- 调用方式:`GET`
- 返回

```
{
  "responseData": [
          {
              "id": 146,
              "name_hiragana": "いとう じゅんな ", //姓名-平假名
              "name_kanji": "伊藤 純奈",          //姓名-汉字
              "birthday": "1998年11月30日",       //生日
              "constellation": "A型",            //血型
              "period": "2期生",                 //几期生
              "stage": "アンダー",               //当前的位置(under或者选拔)
              "height": "165cm",                //身高
              "name_alpha": "itoujunna",        //姓名-字母
              "url": "http://www.nogizaka46.com/member/detail/itoujunna.php", //blog地址
              "avatar": "http://img.nogizaka46.com/www/member/img/itoujunna_prof.jpg" //公式照地址
          },
          ...
   ]
   "code": 200,
   "message": "success"
}
```

##### 4、分页获取成员的信息

- 接口地址:`、member/blogs`
- 调用方式:`GET`
- 参数说明:

  参数名 | 类型 | 必填 | 备注
  --------- | -------------| --------- | -------------
  pageNo | int | 否 | 默认为0（表示第一页）
  pageSize | int | 否 | 默认为15
  nameAlpha | String | 是 | 成员的名字的字母拼写
  
- 返回:
	
	```
	{
	  "content": [
	    {
	      "id": 2366,
	      "author": "中元日芽香",
	      "time": 1485605100,
	      "title": "ご報告",
	      "summary": "\n\t\t先程公式サイトで発表されました、私、中元日芽香は次の17thシングル期間中活動をお休みさせて...\t\t",
	      "url": "http://blog.nogizaka46.com/himeka.nakamoto/smph/2017/01/036690.php",
	      "name_alpha": "nakamotohimeka"
	    },
	    ...
	 ],
	  "last": false,
	  "totalPages": 8,
	  "totalElements": 30,
	  "first": true,
	  "numberOfElements": 4,
	  "size": 4,
	  "number": 0
}
	```















