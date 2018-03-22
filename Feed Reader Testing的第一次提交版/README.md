###成功运行应用程序 所需的所有步骤

1.　用浏览器打开`index.html`文件，即可开始按要求对程序进行测试。

2.　在html文件的最下方，要要顺序设置被测试程序和测试程序的路径
```
        <script src="js/api.js"></script>
        <script src="js/app.js"></script>
        <script src="jasmine/spec/feedreader.js"></script>
        ```

3.　在`Feedreader.js` 中，跟句需求的要求逐一测试了`app.js`的代码。

　　　　第一个`describe`中，最后两个`spec`里面：编写测试对 allFeeds 对象中的每条反馈执行循环操作， 　　　　并确保其具有定义的非空 URL、非空名称。
　　　　
　　　　第二个`describe`中，第一个`spec`里面：编写测试以确保菜单 (menu) 元素在默认情况下处于隐藏状态。
　　　　　　　　　　　　　　　第二个`spec`里面：编写测试，用测试程序触发点击事件模拟点击菜单， 　　　　　　　　　　　　　　　测试菜单是否能改变其可见性。

　　　　第三个`describe`中，编写测试保证 loadFeed 函数被调用而且工作正常。因为`loadFeed()`                         函数是异步的,所以,用 Jasmine 的 `beforeEach`和异步的 `done()`函数实现测试
　　　　
　　　　第四个`describe`中，通过两次调用`loadFeed()`函数分别提取的内容的方式编写测试，确保每当`loadFeed()`　　　　　　　　　　　　　　　函数加载一条新反馈后，内容会相应更改。

