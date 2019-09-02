# UNITOR企业应用框架最小版
提供最基本的框架运行环境及DEMO程序.

详细文档可访问以下地址获得:
http://www.uosgi.com

**1配置JAVA运行环境**

  保证能正常运行JAVA命令,JVM版本建议在1.8或以上.

**2数据库配置**

  加密码数据库密码,新建一个JAVA工程,并加入解压后的 SecurityAPI_1.0.1.jar 包,新建一个类,增加MAIN方法调用加密方法,示例代码如下:
 ```java
  import org.fix.sysbp.security.ag.RSAEncrypt;

  public class EncDemo {//Java
    public static void main(String[] args) {//Java
      String enc = RSAEncrypt.encpwd("123456");//Java
      System.out.println("加密后的密码:"+enc);//Java
    }
  }
 ```
  获得密码后,将其复制到Proxoobundle目录中的mysql.properties 文件中,属性值为:password.
  
**3运行**

  Window:双击 runs/startup.bat .
  Linux:运行 runs/startup.sh .
