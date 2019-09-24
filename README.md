# 2019.9.24
牛客网补充

1.\d:匹配数字字符；\D:匹配非数字字符；\f换页符；\n换行符；\r回车符；\s空白字符；\S非空白字符；\t制表符；\v垂直制表符；\w字母；\W非字母
2.java语言使用的字符码集是Unicode；ASCII是国际上使用最广泛的字符码集；BCD是一种数字压缩存储编码方式
3.虚拟机中没有泛型，只有普通类和普通方法；所有泛型类的类型参数在编译时会被擦除；创建泛型对象时请指明类型，让编译器尽早去做参数检查
4.单例模式的特点：构造方法私有、单一实例；懒汉模式在调用方法时创建对象，恶汉模式在类初始化时创建对象。
  懒汉模式代码：全局单列实例在第一次使用时被构建
  public class Singleton2{
    private static Singleton2 INSTANCE = null;
    private Singleton2(){}
    public static Singleton2 getInstance(){
      if(INSTANCE!=null){
        INSTANCE = new Singleton2();
      }
      return INSTANCE;
    }
  }
  饿汉方式:全局单例实例在类装载时构建
  public class Singleton{
    private final static Singleton INSTANCE = new Singleton();
    private Singleton(){}
    public static Singleton getInstance(){
      return INSTANCE;
    }
  }
5.start是开启线程，run是线程的执行体，run是线程的执行入口；CyclicBarrier和CountDownLatch都是可以让一组线程等待其他线程，前者是让一组线程相互等待到某一个状态再执行，后者是一个线程等待其他线程结束再执行；callable中的call比runnable中run厉害就在于有返回值和可以抛出异常；start把new变成runnable
6.java面向对象语言不容许单独的过程和函数存在，也不允许单独的方法存在
7.run用来执行线程体中具体内容、start用来启动线程、suspend用来挂起
8.当前用户上下文信息session、当前应用application、当前页面pagecontext、当前请求request
9.序列化：将一个具体的对象持久化，写入到硬盘上，静态数据不能被序列化，因为静态数据不在堆内存中，而是在静态方法区中；serializable启动对象序列化；非静态数据不序列化，在网络间传输一些数据
10.数字、字母、下划线、美元符号；首字母不能是数字
11.抽象类可以有构造方法、接口中不能有构造方法；抽象类可以有普通成员变量、接口中没有普通成员变量；
