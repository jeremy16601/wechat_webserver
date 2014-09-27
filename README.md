# Qianduo api

### 1.商户注册
-  http://localhost:3000/api/register_Mer 
-  post方式
-  参数 nickname, password ,tel , alipay, imei 
- 成功：{"success": true}  
- 失败：{"success": false} 

### 2.用户注册
-  http://localhost:3000/api/register
-  post方式
-  参数 nickame, password ,tel , alipay ,imei
- 成功：{"success": true}  
- 失败：{"success": false} 

### 3.商户列表
- http://localhost:3000/api/userList_Mer
- 请求方式 get 

### 4.用户列表
- http://localhost:3000/api/userList
- 请求方式get

### 5.用户登陆
- http://localhost:3000/api/userLogin
- post方式
- 参数 nickname,password
- 成功：{"success": true}  
- 失败：{"success": false} 

### 6.商户登陆
- http://localhost:3000/api/merLogin
- post方式
- 参数 nickname,password
- 成功：{"success": true}  
- 失败：{"success": false} 

### 7.根据用户名得到用户详细信息
- http://localhost:3000/api/userFindByName?nickname=用户名
- get方式
- 参数nickname
- 成功返回用户详细信息
- 失败{"data":"暂无数据！"}

### 8.根据商户名得到商户详细信息
- http://localhost:3000/api/userFindByName_Mer?nickname=用户名
- get方式
- 参数nickname
- 成功返回用户详细信息
- 失败{"data":"暂无数据！"}

### 9.根据用户_id 修改用户信息
- http://localhost:3000/api/userEdit
- post方式
- 成功返回{"success": true}
- 失败{"success": false}

### 10.根据商户_id 修改商户信息
- http://localhost:3000/api/userEdit_Mer
- post方式
- 成功返回{"success": true}
- 失败{"success": false}


### 11.商户发布广告
- http://localhost:3000/api/addAds
- post方式 (参数按照文档顺序)
- 参数：{nickname,ad_type,ad_image,ad_title,pro_name,phone,mer_href,pro_detail,pro_oldprice,pro_price,sing_price,pub_time(不需要传入),count,days}
- 成功返回{"success": true}
- 失败{"success": false}

### 12.所有广告列表
- http://localhost:3000/api/mer_AdsList
- get方式

### 13.根据商户nickname 查询该商户发布的广告
- http://localhost:3000/api/adsFindByName?nickname=XXX
- post方式
- 参数:nickname 
- 成功返回数据列表

### 14. 检测版本更新
- http://localhost:3000/api/update
- get方式
- 成功返回{"path": "ip:3000/qianduo.apk","version": "1"} 
- path是apk下载路径，可以放到任何地方，到时候提供给我地址就可以，
- android每次检测version，和AndroidManifest.xml 里的版本号是否一致，用来做更新判断；

### 15. 顶部广告列表
- http://localhost:3000/api/adsTopList
- get方式

### 16. 添加顶部广告
- http://localhost:3000/api/addTopAds
- post方式
- 参数：img_path ,img_href 
- 成功返回{"success": true}
- 失败{"success": false}

### 17. 获取转发人全部列表
- http://localhost:3000/api/forwardUserList
- get方式

### 18. 存储转发人
- http://localhost:3000/api/addForwardUsers
- post方式
-参数 转发人昵称：f_nickname，广告ID：f_adsID ，广告分类ID ：f_adsType
- 成功返回{"success": true}
- 失败{"success": false}

### 19. 根据广告id 查询转发人列表
- http://localhost:3000/api/forwardListByAdsID?adsID=xxx
- get方式 参数：adsID
- 成功返回数据列表
