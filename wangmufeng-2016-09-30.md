# 2016-09-30工作日报
=====================

1. 已完成工作
    * JDBC
2. 工作成果
  * JDBC
  * build.gradle 文件 在dependencies下增加 compile 'mysql:mysql-connector-java:5.1.39'
  * 查询

```
import java.sql.*;

import static java.lang.Class.forName;

/**
 * Created by Administrator on 2016/9/30.
 */
public class JDBCTest {
    public static void main(String[] args) {
    	//固定格式
        String driver = "com.mysql.jdbc.Driver";
        String url = "jdbc:mysql://localhost:3306/wangmufeng_db?useUnicode=true&characterEncoding=utf-8&useSSL=false";
        String username = "root";
        String password = "ykq92";
        try {
            forName(driver);
            Connection connection = DriverManager.getConnection(url, username, password);
            

            StringBuffer sb = new StringBuffer();
            //注意空格
            sb.append("SELECT                       ");
            sb.append("id,name,sex,birthday,password ");
            sb.append("FROM                         ");
            sb.append("user_                        ");
//            sb.append("WHERE                        ");
//            sb.append("name = '王目峰';             ");
//            System.out.println(sb.toString());
            Statement st = connection.createStatement();
            ResultSet rs = st.executeQuery(sb.toString());

			//循环输出
            while (rs.next()) {
                int id = rs.getInt("id");
                String name = rs.getString("name");
                System.out.println(id + ";" + name);
            }


        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        } catch (SQLException e) {
            e.printStackTrace();
        }

    }

}
```
3. 未完成工作
    * JDBC与数据库未完成链接
4. 未完成原因
    * 
5. 遇到问题及解析
