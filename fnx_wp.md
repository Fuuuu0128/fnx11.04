###  2017-11-04


# Buy me a Tesla
#### 0x00 [原理]
     base64,url编码
#### 0x01 [目的]
     了解服务器url参数的编码解码,base64
#### 0x02 [环境]
     windows
#### 0x03 [工具]
     Chrome,Burpsuite
#### 0x04 [步骤]

1.首先打开分析题目，提示使用Burpsuite抓包

![](/files_for_wp/buy1.png)

2.在url栏输入http://222.18.158.196:2004/index.php，打开网页，点击购买，提示余额不足

![](/files_for_wp/buy2.png)

3.F12，打开页面元素

![](/files_for_wp/buy3.png)

4.查找关键字（Ctrl+f）：submit

![](/files_for_wp/buy4.png)

5.##  三次base64解码

![](/files_for_wp/buy5.png)

![](/files_for_wp/buy6.png)

![](/files_for_wp/buy7.png)

得到解码结果：teslaModelX{value:1602500,{users's yue:10}

6.修改金额：大于1700000</br>

teslaModelX{value:1602500,{users's yue:1700000}</br>

将结果再三次编码:</br>
![](/files_for_wp/buy8.png)

![](/files_for_wp/buy9.png)

![](/files_for_wp/buy10.png)</br>

编码结果为：WkVkV2VtSkhSazVpTWxKc1lrWm9OMlJ0Um5Oa1YxVTJUVlJaZDAxcVZYZE5RM2czWkZoT2JHTnVUVzVqZVVJMVpGZFZOazFVWTNkTlJFRjNUVWd3UFE9PQ==

7.flag：

![](/files_for_wp/buy11.png)

#### 0x05 [总结]
    base64,url编码
</br>
</br>
</br>
</br>
</br>






