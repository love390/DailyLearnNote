1.本次重新回顾，重新熟悉Junit的注解，了解新注解@Rule;
 （*）@Rule注解,可以通过实现TestRule来对方法做切面，在@Test方法运行前后加入自定义代码（*）
        Junit也提供了一些默认Rule,如下：
          TemporaryFolder Rule：创建一些临时目录或者文件
          ExternalResource Rule：ExternalResource 是TemporaryFolder的父类，主要用于在测试之前创建资源，并在测试完成后销毁
          ErrorCollector Rule：收集多个错误，并在测试执行完后一次过显示出来
          Verifier Rule：是ErrorCollector的父类，可以在测试执行完成之后做一些校验，以验证测试结果是不是正确
          TestWatcher Rule：定义了五个触发点，分别是测试成功，测试失败，测试开始，测试完成，测试跳过，能让我们在每个触发点执行自定义的逻辑
          TestName Rule：能让我们在测试中获取目前测试方法的名字
          Timeout与ExpectedException Rule：分别用于超时测试与异常测试
     （*）特别的，SpringBoot提供了OutputCapture：用来取出测试方法执行过程的日志
             我写了个自定义rule结合OutputCapture来统计查询语句数量，循环控制及总运行时间
    @After,@AfterClass,@Before,@BeforeClass,@Test,@RunWith简单，只是进行回顾
2.使用Junit进行模拟登录后的Web接口测试
      （*）需要用到MockMvc来进行Web接口测试
             需要进行初始化——>
                注入WebApplicationContext
                初始化方法中(@Before)：this.mockMvc = MockMvcBuilders.webAppContextSetup(this.wac).apply(springSecurity()).build();
      （*）权限相关：
               使用@WithMockUser等系列注解模拟登录
3.使用Junit进行高并发测试
