#2016-10-14工作日报
===================

1. 已完成工作
    * 使用IntelliJ做新增和查询
2. 工作内容
    *  新增
        * package com.feicuiedu.daily.controller;
          import com.feicuiedu.daily.uitl.DBUtils;
          import java.text.SimpleDateFormat;
          import java.util.Date;
          import java.util.Scanner;
          
          
            Created by Administrator on 2016/10/14.
           
          public class write {
              public static void writeDaily()  {
             Scanner sc = new Scanner(System.in);
      
      
             System.out.println("请输入日报名称：");
             String name = sc.next();
             System.out.println("应完成工作:");
             String inputSFW = sc.next();
             System.out.println("已完成工作:");
             String inputHFW = sc.next();
             System.out.println("未完成原因:");
             String inputReason = sc.next();
             System.out.println("遇到问题:");
             String inputQAA = sc.next();
             System.out.println("明日计划:");
             String inputNDP = sc.next();
             SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
             String date = sdf.format(new Date());
             SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy-MM-dd");
             String date2= sdf2.format(new Date());
             StringBuffer sb = new StringBuffer();
             sb.append("insert into daily(name)values");
             sb.append("insert into daily(create_date)values");
             sb.append("insert into daily(should_finished_work)values");
             sb.append("insert into daily(have_finished_work)values");
             sb.append("insert into daily(unfinished_work_reason)values");
             sb.append("insert into daily(question_and_answer)values");
             sb.append("insert into daily(next_day_plain)values,(\"");
             sb.append(name+"-"+ date2 +"  日报\",\" ");
             sb.append(date+" \",\" ");
             sb.append(inputSFW+" \",\" ");
             sb.append(inputHFW+" \",\" ");
             sb.append(inputReason+" \",\" ");
             sb.append(inputQAA+" \",\" ");
             sb.append(inputNDP+"\" ) ");
      
             DBUtils.modifyTable(sb.toString());
      
             System.out.println("日报存入");
    }
}

   *  查询
      *  package com.feicuiedu.daily.pojo;

import com.feicuiedu.daily.uitl.DBUtils;

import java.util.List;
import java.util.Map;

/**
 * Created by Administrator on 2016/10/14.
 */
public class daily {
    public static void getDaily() {

        String strSql = "select * from  `daily_`";
        List<Map<String,Object>> list = DBUtils.queryTable(strSql);

        for (Map<String,Object> map:list) {
            for (Map.Entry<String,Object> entry : map.entrySet()) {
                String key = entry.getKey();
                Object value = entry.getValue();
                System.out.print(key+":"+value+",");
            }

            System.out.println();
        }
    }
}


3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
