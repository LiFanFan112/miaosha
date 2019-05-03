
# SpringBoot基础电商秒杀项目

# 项目简介

## 通过SpringBoot快速搭建的前后端分离的电商基础秒杀项目。使用MyBatis对数据库MySQL进行操作。
### 项目通过应用领域驱动型的分层模型设计方式去完成：用户注册、登陆、查看、商品列表、进入商品详情、下单购买以及倒计时秒杀开始后下单购买的基本流程。

## 基本要点

1 使用Mybatis-generator自动生成MyBatis配置文件以及DataObject

2 统一前端返回格式

CommonReturnType {status: xx ,object:xx} 

dataobject -> 与数据库对应的映射对象 model -> 用于业务逻辑service的领域模型对象 

viewobject -> 用于前端交互的模型对象

3 使用 hibernate-validator 通过注解来完成模型参数校验

4 出现异常时统一抛出至controller层由@ExceptionHandler统一处理

5 使用聚合模型在itemModel加入PromoModel promoModel，若不为空表示其有未结束的秒杀活动；在orderModel中加入promoId，若不为空，则以秒杀方式下单
