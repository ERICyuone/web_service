# web_service
#########工程的基本功能
本工程用于后端数据的处理与发布

#########部署步骤
1、Windows7 64位环境下，安装JDK1.8.202，由于安装JDK较为简单，提供以下链接参考安装。
http://baijiahao.baidu.com/s?id=1599433496793814200&wfr=spider&for=pc

2、Windows7 64位环境下，使用IntelliJ IDEA.2017软件进行编译	
（1）IntelliJ IDEA.2017的安装
1）进入官网下载IntelliJ IDEA  
https://www.jetbrains.com/idea/download/#section=windows 进入官网下载 
左边为旗舰版是收费的，右边是社区版是免费的，我们选择旗舰版的下载之后可破解 
 
2）下载之后进行安装，next 
 
3）选择java，因为本工程使用java编写程序。
 
4）安装完成之后进行启动即可 
 
5）导入之前的配置，以前安装过的选择上面一项 
 






6）接受条款 
 
7）接下来就是破解了 
 
破解
1、下载破解补丁JetbrainsCrack-2.6.2.jar 地址: 
http://download.csdn.net/detail/gnail_oug/9824630或者http://idea.lanyus.com/

2.将你下载好的JetbrainsCrack-2.6.2.jar拷贝到你的Idea安装目录的bin目录 下,如下图红色框所示
 
3.在安装的idea下面的bin目录下面有2个文件 ： 一个是idea64.exe.vmoptions，还有一个是idea.exe.vmoptions（如上图绿框）。

用记事本打开 分别在最下面一行增加一行：-javaagent:**G:\IDEA**\bin\JetbrainsCrack-2.6.2.jar

注意:“G:\IDEA是对应的JetbrainsCrack-2.6.2.jar的安装位置,你用你自己的安装路径。

4.重新启动软件,再到Acrivation code中选择界面的时候,写入下面注册代码
ThisCrackLicenseId-{      
    "licenseId":"ThisCrackLicenseId",     
    "assigneeName":"",     
    "assigneeEmail":"idea@163.com",      
    "licenseRestriction":"For This
    Crack, Only Test! Please support   genuine!!!",     
    "checkConcurrentUse":false,      "products":[     
    {"code":"II","paidUpTo":"2099-12-31"},     
    {"code":"DM","paidUpTo":"2099-12-31"},     
    {"code":"AC","paidUpTo":"2099-12-31"},     
    {"code":"RS0","paidUpTo":"2099-12-31"},     
    {"code":"WS","paidUpTo":"2099-12-31"},    
    {"code":"DPN","paidUpTo":"2099-12-31"},    
    {"code":"RC","paidUpTo":"2099-12-31"},     
    {"code":"PS","paidUpTo":"2099-12-31"},    
    {"code":"DC","paidUpTo":"2099-12-31"},     
    {"code":"RM","paidUpTo":"2099-12-31"},     
    {"code":"CL","paidUpTo":"2099-12-31"},     
    {"code":"PC","paidUpTo":"2099-12-31"}      ],     
    "hash":"2911276/0",      
    "gracePeriodDays":7,
"autoProlongated":false}   
 
3、使用Navicat Premium 12 来对数据库进行可视化操作，此软件不是本工程运行的必要软件，仅对开发人员提供调试的便利性，因此选择性安装。安装过程参考以下链接。
https://www.jianshu.com/p/5f693b4c9468

4、打开工程，若运行有错误，可以考虑是否工程的配置出现了问题。
打开
  
 
 
参考以上配置。

5、工程运行后，可观察到IDEA控制台出现
 
证明工程正常运行，并且已经将端口发布出去，数据库的数据插入以及更新正常。
6、工程运行后，打开cmd界面
    1）将路径cd到需要发布到的客户端（前端页面）工程的src文件夹下
        如：e:\$path1\javaproject\src>
    2）找到publish.bat（该文件在web_service文件下）的路径$path2，输入 start e:\$path2\publish.bat 等待脚本运行完即可。
 
7、在客户端（前端页面）的工程即可以调用后端提供的方法。




















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
