# Macula

## Dec 30th, 2015

1.  应用加载时，将通过扫描classpath路径：org.macula.core.config目录，并实现了ConfigurationProvider接口的Bean，来修改Configuration信息。

    如org.macula.core.config.PropertyConfigurationProvider就是通过读取macula.properties来读取macula平台Configuration信息的处理