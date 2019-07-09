#########软件的基本功能
本软件用于后端数据的处理与发布

#########部署步骤
（1）Windows环境下，使用IDEA打开工程，若有错误，可以考虑是否工程的配置出现了问题。
（2）工程运行后，打开cmd界面
    1）将路径cd到需要发布到的客户端工程的src文件夹下
        如：e:\$path1\javaproject\src>
    2）找到publish.bat的路径$path2，输入 start e:\$path2\publish.bat 等待脚本运行完即可。

#########目录结构描述
本工程代码结构分为三层
    1）dao：读写取数据库数据的方法。
    2）service：对读取到的数据库数据或前端发来的数据进行处理。
    3）server：对处理好的数据存储好，通过端口发布出去供前端使用。
    其中：entity：定义数据的类。database：定义操作数据库的方法。
     
    ├─.idea                       // 工程在idea运行后产生
    │  ├─dataSources            
    │  ├─inspectionProfiles
    │  └─libraries
    ├─lib                         // 使用到的jar包
    ├─out                         // idea运行后产生
    │  └─production
    │      └─web_service
    │          ├─dao
    │          │  └─impl
    │          ├─database
    │          ├─entity
    │          ├─server
    │          └─service
    │              └─impl
    └─src                         // 工程根目录
        ├─dao                     // 读写取数据库数据的方法
        │  └─impl                 // 方法实现
        ├─database                // 定义操作数据库的方法
        ├─entity                  // 定义数据的类
        ├─server                  // 要发布方法定义
        └─service                 // 处理数据的方法
            └─impl                // 方法实现
  
####To-do List
- 1：多因数的判别
- 2：多因数异常数据库的存储
