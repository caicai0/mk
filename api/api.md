1. 统一名称

	|名称 |含义|备注|
	|--- |---|---|
	|id|唯一标识
	|title|标题|
	|source|来源|
	|views|浏览量，阅读数
	|image|图片
	|type|类型|一般情况下用整数类型的自然数，并且0一般情况下表示默认类型
	|price|价格|整数类型，单位：分
	|label|标签
	|article|文章|资讯内容的基本单元，包括短视频
2. 数据类型定义
	1. 文章：官方或UGC发布的html文本、图片、音频或视频。作为资讯存在。 
		1. 资讯列表item
		2. <a name="历史列表文章">历史列表文章item</a>
		
			|属性 |类型|含义|备注|
			|--- |---|---|---|
			|id|Int|唯一标识
			|title|String|标题|
			|source|String|来源|
			|views|Int|浏览量，阅读数
			|image|String|图片
		3. 
3. 接口定义
	1. 历史接口：用户浏览过内容的记录
		1. url：http://116.213.204.11:8081/appserver/phone/communal4_history.xhtml
		2. method：GET
		3. 参数列表
		
			|参数 |类型|含义|备注|
			|--- |---|---|---|
			|page|Int|页码
			|pushtime|Longlong|时间戳|
		4. 返回值列表
				
			|属性 |类型|含义|备注|
			|--- |---|---|---|
			|code|Int|成功，或失败标号
			|message|String|说明
			|datas|Array|内部类型：<a href="#历史列表文章">历史列表item</a>|
4. 锚点
	1. 历史列表文章