# QG训练营移动组第五周周记 2019年4月15日
## 一、生活随记
### 6/1 星期一
#### 一、学习第一行代码
* ***配置litepal***
    1. 添加依赖
    2. 编辑litepal.xml文件
    ```
    <?xml version="1.0" encoding="utf-8"?>
    <litepal>
        <dbname value="BookStore"></dbname>
        
        <version value="1"></version>
        
        <list>
        </list>
    </litepal>
    ```
    3. 修改AndroidManifext.xml文件
* ***创建和升级数据库***
    1. 创建一个类
    2. 将该类添加到映射模型
    3. 调用LitePal.getDataBase()创建数据库和表
    4. 升级库：做相应修改后对版本号+1
* ***LitePal添加数据***
    1. 继承DataSupport(android studio提示错误，查看了LitePal最新文档发现得继承LitePalSupport)
    2. save就对了
* ***LitePal更新数据***
    1. 对已存储对象进行更改（更改完save就对了）
    2. 利用updataAll进行更改
* ***LitePal删除数据***
    1. 对已存储对象删除（delete就完事了）
    2. 使用静态方法（LitePal.deleteAll等）
* ***LitePal查询数据(LietPal.findAll)***
* ***LitePal比SQLite方便许多...***
***
#### 二、穿插学点swing
#### 三、回来学android
* ***运行时权限***
    1. 在AndroidManifest.xml中注册权限
    2. 检查手机权限是否允许使用该权限
    3. 弹出提示信息询问用户是否允许开启权限
* ***访问其他程序中的数据***
    1. 通过getContentResolver()获得ContentResolver
    2. 利用ContentResolver进行CRUD(和SQLite几乎一样，注意把表名改为Uri对象)
### 6/2 星期二
#### 一、学习第一行代码
* ***创建自己的内容提供器***
    1. 继承ContentProvider
    2. 重写六个抽象方法
        1. onCreate()
        2. query()
        3. insert()
        4. updata()
        5. delete()
        6. getType()
    3. 借助UriMatcher对象的addUri匹配URI功能
    4. gettype()返回对应的MIME类型
* ***使用通知***
    1. 创建NotificationManager对象
    2. 构建Notification对象
    3. 用notify方法让通知显示出来
    4. 按书上代码敲完以后点击按钮，消息栏并没有显示通知
    5. 解决方案[https://blog.csdn.net/guolin_blog/article/details/79854070]
### 6/3 星期三
#### 一、学习第一行代码
* ***播放音频***
    1. 创建MediaPlayer对象
    2. 调用setDataSource()设置路径
    3. 调用prepare()使MediaPlayer进入准备状态
    4. 调用start()开始播放音频
* ***播放视频***
    1. 在布局中放置VideoView控件
    ```
    <VideoView
    android:id="@+id/..."
    android:layout_width="..."
    android:layout_height="...." />
    ```
    2. 调用setVideoPath()设置路径
    3. 调用start()方法播放视频
* ***WebView***
* ***使用httpURLConnection***
    1. 创建HttpURLConnection实例
        1. new一个URL对象
        2. 调用openConnection方法(url.openConnection())
    2. 设置HTTP请求所使用的方法（get或post）
    3. getInputStream获得输入流
    4. disconnect关闭HTTP连接
* ***解析XML格式的数据***
    1. Pull解析方式
        1. 获取XmlPullParserFactory的实例
        2. 借助该实例获得XmlPullParser
        3. 调用setInput设置XML数据
        4. getEventType()可以得到当前的解析事件
    2. SAX解析方式
### 6/4 星期四
#### 一、学习第一行代码
* ***异步消息处理机制***
    1. 在主线程中创建Handle并重写HandleMessage方法
    2. 在子线程中创建Message对象
    3. 将Message用Handle对象的sendHandle方法发生出去
    4. Message会在MessageQueue中等待处理
    5. Looper会将MessageQueue中信息取出并传入HandleMessage
* ***使用AsyncTask***
    1. onPreExecute()
    2. doInBackground()
    3. onProgressUpdate()
    4. onPostExecute()
* ***服务***
    1. 第一次创建服务会调用onCreat()
    2. 启动服务会调用onStartCommand()
    3. 销毁服务调用onDestory()
* ***在活动中绑定服务***
    1. 在服务中创建binder子类
    2. 创建该子类的对象
    3. 在活动中创建ServiceConnection对象
    4. 绑定服务与解绑服务
* ***服务的生命周期***
### 6/5 星期五
* ***大组培训***
* ***学点Material Design(一点点)***
### 6/6 星期六
### 6/7 星期天
* ***都在盰作业***
## 二、一周总结
***这个星期一直都在学习第一行代码，学习的进度还算可以，有好几个晚上跑去24小时书吧，也是到了很晚才回宿舍，不过回来后总是失眠，影响了睡眠的质量。但学习的效率还是比较高的，不过知识容易遗忘，学得太快也要多回去复习才行呐...***
## 三、存在问题
* ***睡眠质量差，多多少少有些影响效率***
* ***下了一整星期的雨，几乎都没去运动***
* ***知识遗忘率较高，需要安排时间复习***
* ***忙到还没时间剪头发***
## 四、下周计划
* ***一边学习一边复习一边完成小组作业***
* ***复习点java***

