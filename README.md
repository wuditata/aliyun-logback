# aliyun-logback

logback日志组件与阿里云日志服务的结合

```xml
<appender name="aliyun" class="com.hwc.aliyun.logback.AliyunLogbackAppender">
    <projectName>projectName</projectName>
    <logstore>logstoreName</logstore>
    <topic>topicName</topic>
    <accessKeyId></accessKeyId>
    <accessKey></accessKey>
    <endpoint>cn-[地域]-intranet.log.aliyuncs.com</endpoint>
    <timeFormat>yyyy-MM-dd HH:mm:ss</timeFormat>
    <timeZone>PRC</timeZone>
</appender>
```

```xml
<springProfile name="product">
    <root level="INFO">
        <appender-ref ref="CONSOLE"/>
        <appender-ref ref="aliyun"/>
    </root>
</springProfile>
```