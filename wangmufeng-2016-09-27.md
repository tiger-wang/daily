## **2016年9月27日**

***

## 1.已完成内容
    * Java集合框架包含的内容
      * Collection
        * List
        * Set
      * Map
***

 ## 2.工作成果



```java
import java.util.ArrayList;

import java.util.Iterator;

import java.util.List;

public class ListDemo {

public static void main(String[] args) {

// 创建
List<String> list = new ArrayList<String>();

// 添加
list.add("毛泽东");

list.add("周恩来");

list.add("刘少奇");

list.add(2,"朱德");

// list.add("林彪");

//  修改
// list.set(0,"林彪");			
// 删除
// list.remove(0);
list.remove("毛泽东");

// 查询遍历
			for(int index = 0;index< list.size();index ++) {
				String name = list.get(index);
				System.out.println(name);
			}

			System.out.println("*******************************");
			for (String name : list) {
				System.out.println(name);
			}

			System.out.println("*******************************");
			Iterator<String> it = list.iterator();
			while(it.hasNext()) {
				String name = it.next();
				System.out.println(name);
			}
		}
	}
```



***

## **3.未完成工作**

​		**无**

------

## **4.未完成原因**

​		**无**

------

## **5.遇到的问题及解决方案**

​		**无**
