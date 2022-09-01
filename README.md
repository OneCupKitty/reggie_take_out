# reggie_take_out
## 初始原型
### 技术架构
springboot + vue.js
## v1.0 
### 技术架构
#### 使用Redis 
将手机端验证码存储到Redis
查询菜品信息,先到Redis中查询,若没有,再到mysql查询,并将数据存放到Redis中
增加,修改菜品信息后,删除Redis中的数据.
#### 使用spring cache 简化Redis的操作
@CacheEvict 在修改数据库的方法上,作用:删除Redis数据
@Cacheable 在查询数据库的方法上,作用:查看Redis是否有数据,有则直接返回.没有则查询,并将数据保存到Redis
## v1.1
### 技术架构
#### 使用mysql 实现 主从复制,读写分离
## v1.2
### 技术架构
#### 使用Nginx 部署前端静态资源,并实现反向代理,(由于只有一个服务器,故没有实现负载均衡)
#### 使用swagger 根据后端代码,生成接口文档
