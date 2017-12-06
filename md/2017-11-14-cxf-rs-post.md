#rs远程调用

RSSubscriptionConfigService
RSSubscriptionConfigServiceImpl

1.rsProxy类实现 service接口,并将rxProxy代理类以.xml配置为csf客户端的方式提供给调用项目(一般在被调项目的rsService.xml中配置)
  <bean id="dpos-auth-api.subscriptionConfigService" class="com.hd123.dpos.auth.rs.proxy.notification.SubscriptionConfigServiceProxy"
        p:codecBean-ref="dpos-auth-api.codecBean" p:service-ref="dpos-auth-api.rs.subscriptionConfigService"/>        

2.写RSService接口,
2.rsProxy类的方法实现实际上是对RSService的封装

3.在被调用项目配置rs服务端,将RSImpl配置给cxf服务端
      <bean class="com.hd123.dpos.auth.rs.service.notification.RSSubscriptionConfigServiceImpl"
        p:service-ref="subscriptionConfigServiceImpl"
        p:codecBean-ref="dpos-auth-service.codecBean" />