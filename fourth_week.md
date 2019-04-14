# QG训练营移动组第四周周记 2019年4月8日
## 生活随记
### 5/1
#### 一、复习java基础（记录一些容易忘的）
* ***形参个数可变的方法***
```
public class Varargs
{
    public static void test(int a,String...books)
    {
        for(String tmp:books)
        {
            System.out.println(tmp);
        }
        
        System.out.println(a);
    }
    public static void main(String[] args)
    {
        test(5,"java","android");
    }
}
```
***说明:个数可变的形参只能处于形参列表的最后***
* ***不能使用方法返回值类型作为区分方法重载的依据***
#### 二、学习第一行代码
##### ***滚动控件----RecyclerView***
* ***添加依赖：implementation'com.android.support:recyclerview-v7:28.0.0'***
* ***为RecyclerView准备一个适配器(继承至RecyclerView.Adapter)***
* ***适配器内定义一个内部类ViewHolder***
* ***重写适配器的构造方法***
* ***重写onCreateViewHolder,onBindViewHolder,getItemCount方法***
* ***书P123-P124***
### 5/2 星期二
#### 一、复习java基础（记录一些容易忘的）
* ***instanceof用于判断前面的对象是否是后面的类，或者其子类，实现类的实列***
* ***没什么好记的了？***
#### 二、学习第一行代码
* ***碎片的生命周期（类似于活动）***
    1. 运行状态
    2. 暂停状态
    3. 停止状态
    4. 销毁状态
    5. 特别的：
        1. onAttach();
        2. onCreateView();
        3. onActivityCreated();
        4. onDestroyView();
        5. onDetach();
        
#### 三、学习SQL和JDBC编程
* ***SQL语句***
```
 craete database <库名>;
 show databases;
 drop database <库名>;
 use <库名>;
 create table <表名>(
    ........
 );
 show tables;
 desc <表名>;
 drop table <表名>;
 insert into <table>(....)
 values(....);
 
 insert into <table>(....)
 values(....),(....),(....).....;
 
 update <table>
 set....;
 
 delete from <table>
 (where....);
 
 select * from <table> (where...);
 select .... from <table> (where....);
```
* ***几种特殊运算符***
```
    select * from <table>
    where ... between val1 and val2;
    
    select * from <table>
    where ... in(val1,val2);
    
    #类似，还有...
    where ... like ' ';
    where ... is null;
    where ... and ...;
    where ... or ...;
    where not ...;
```
* ***JDBC编程步骤***
    1. 加载数据库驱动
    2. 通过DriverManager获取数据库连接
    3. 通过Connection对象创建Statement对象
    4. 使用Statement执行SQL语句
    5. 操作结果集
    6. 回收数据库资源
### 5/3 星期三
#### 一、学习第一行代码
* ***创建广播接收器(继承Broadcast,重写onReceive)***
* ***动态注册监听对象***
    1. 创建IntentFilter,设置监听对象
    2. 创建广播接收器
    3. registerReceiver完成注册
    4. 在活动的onDestory注销广播接收器
* ***静态注册监听对象***
    ```
    <receiver
    android:name="...."
    .....>
    </receiver>
    ```
* ***发送自定义广播***
    1. 创建Intent对象
    2. sendBroadcast(Intent对象)发送广播

#### 二、继续复习java

### 5/4 星期四
* ***topview分享会***
* ***看了一点第一行代码***
### 5/5 星期五
* ***大组培训***
* ***学习awt编程(尽管没用...)***
* ***搞了一晚javafx，总是抛异常，估计是JDK版本的原因***
### 5/6 星期六
* ***学点Swing(虽然没用...)***
* ***盰作业***
### 5/7 星期日
* ***看了点SQLite***
* ***继续盰作业***
## 一周总结
***android studio这周还没有发生什么奇怪的问题，学android挺顺利的，进度也慢慢跟上来了。这一周还是很忙（这个学期哪个星期不忙的...）。比起上学期偶尔学习完了还有休息的时间，这个学期从头到尾都在学习和写作业，希望自己能够坚持下去***
## 存在问题
* ***知识遗忘速度有点高***
* ***效率还可以再高些***
## 下周计划
* ***定个小目标：第一行代码看到12章***
* ***继续复习java***

