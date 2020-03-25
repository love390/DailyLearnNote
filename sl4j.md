## SL4J相关
#### 设置变量
   springProperty: 可引用application.yaml的配置
   property: 设置变量
### MDC
   MDC是用于对日志系统固定的变量如%LEVEL等的扩展,在将自定义变量放入MDC后,可通过"%X"获取，如key为"test"时，其对应PATTERN为"%X{test:-}",其中":-"非必须
