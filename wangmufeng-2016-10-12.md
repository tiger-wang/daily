#2016-10-12工作日报
===================


1. 已完成工作
   * 使用androidstudio设计登录界面和使用androidstudio里面RelativeLayout设计计算机器界面
2. 工作内容
    *  <?xml version="1.0" encoding="utf-8"?
    *    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    *    xmlns:app="http://schemas.android.com/apk/res-auto"
    *    android:layout_width="match_parent"
    *    android:layout_height="match_parent"
    *    android:orientation="vertical">
    *    <Button
    *        android:id="@+id/a5"
    *        android:layout_width="200dp"
    *        android:layout_height="wrap_content"
    *        android:layout_alignParentBottom="true"
    *        android:text="登录" />
    *    <Button
    *        android:id="@+id/a6"
    *        android:layout_width="200dp"
    *        android:layout_height="wrap_content"
    *        android:layout_alignParentBottom="true"
    *        android:layout_toRightOf="@+id/a5"
    *        android:text="注册" />
    *    <CheckBox
    *        android:id="@+id/a3"
    *        android:layout_width="wrap_content"
    *        android:layout_height="wrap_content"
    *        android:layout_above="@+id/a5"
    *        android:layout_alignLeft="@+id/a2"
    *        android:layout_alignStart="@+id/a2"
    *        android:layout_marginBottom="23dp"
    *        android:text="记住密码"
    *        android:textSize="30dp" />
    *    <TextView
    *        android:id="@+id/a4"
    *        android:layout_width="wrap_content"
    *        android:layout_height="wrap_content"
    *        android:layout_alignBaseline="@+id/a3"
    *        android:layout_alignBottom="@+id/a3"
    *        android:layout_toEndOf="@+id/a5"
    *        android:layout_toRightOf="@+id/a5"
    *        android:text=" 忘记密码"
    *        android:textSize="30dp" />
    *    <TextView
    *        android:id="@+id/a2"
    *        android:layout_width="match_parent"
    *        android:layout_height="wrap_content"
    *        android:layout_above="@+id/a3"
    *        android:layout_alignParentEnd="true"
    *        android:layout_alignParentRight="true"
    *        android:layout_marginBottom="49dp"
    *        android:text="     密码:____________"
    *        android:textSize="30dp" />
    *    <TextView
    *        android:id="@+id/a1"
    *        android:layout_width="match_parent"
    *        android:layout_height="wrap_content"
    *        android:layout_alignEnd="@+id/a4"
    *        android:layout_alignRight="@+id/a4"
    *        android:layout_centerVertical="true"
    *        android:text="用户名:____________"
    *        android:textSize="30dp" />
    *    <TextView
    *        android:layout_width="match_parent"
    *    android:layout_height="wrap_content"
    *    android:text="日报登录系统"
    *    android:textSize="50dp" />
    *  </RelativeLayout>
    *  ![001](image/demo1.jpg)
    **** 使用androidstudio里面RelativeLayout设计计算机器界面
    *   <?xml version="1.0" encoding="utf-8"?>
    *  <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    *  android:layout_width="match_parent"
    *  android:layout_height="match_parent">
    *  <TextView
    *      android:id="@+id/t"
    *      android:layout_width="match_parent"
    *      android:layout_height="200dp"
    *      android:background="#00aa00"
    *      android:text="请输入："
    *      android:textSize="60dp"/>
    *  <Button
    *      android:id="@+id/a1"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:layout_below="@+id/t"
    *      android:text="MC"/>
    *  <Button
    *      android:id="@+id/b1"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="1"
    *      android:layout_below="@+id/a1"/>
    *  <Button
    *      android:id="@+id/c1"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="4"
    *      android:layout_below="@+id/b1"/>
    *  <Button
    *      android:id="@+id/d1"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="7"
    *      android:layout_below="@+id/c1"/>
    *  <Button
    *      android:id="@+id/e1"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="+"
    *      android:layout_below="@+id/d1"/>
    **  <Button
    *      android:id="@+id/a4"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="M-"
    *      android:layout_below="@+id/t"
    *      android:layout_toRightOf="@+id/a3" />
    *  <Button
    *      android:id="@+id/b4"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="/"
    *      android:layout_below="@+id/a4"
    *      android:layout_toRightOf="@+id/b3" />
    *  <Button
    *      android:id="@+id/c4"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="*"
    *      android:layout_below="@+id/b4"
    *      android:layout_toRightOf="@+id/c3"/>
    *  <Button
    *      android:id="@+id/d4"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="-"
    *      android:layout_below="@+id/c4"
    *      android:layout_toRightOf="@+id/d3" />
    *  <Button
    *      android:id="@+id/a3"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="M+"
    *      android:layout_below="@+id/t"
    *      android:layout_toRightOf="@+id/a2"
    *      android:layout_toEndOf="@+id/a2"
    *      android:layout_marginLeft="15dp"
    *      android:layout_marginStart="15dp" />
    *  <Button
    *      android:id="@+id/b3"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="3"
    *      android:layout_below="@+id/a3"
    *      android:layout_alignLeft="@+id/a3"
    *      android:layout_alignStart="@+id/a3" />
    *  <Button
    *      android:id="@+id/c3"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="6"
    *      android:layout_below="@+id/b3"
    *      android:layout_alignLeft="@+id/b3"
    *      android:layout_alignStart="@+id/b3" />
    *  <Button
    *      android:id="@+id/d3"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="9"
    *      android:layout_below="@+id/c3"
    *      android:layout_alignLeft="@+id/c3"
    *      android:layout_alignStart="@+id/c3" />
    *  <Button
    *      android:id="@+id/a2"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="MR"
    *      android:layout_below="@+id/t"
    *      android:layout_toRightOf="@+id/a1"
    *      android:layout_toEndOf="@+id/a1"
    *      android:layout_marginLeft="10dp"
    *      android:layout_marginStart="10dp" />
    *  <Button
    *      android:id="@+id/b2"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="2"
    *      android:layout_below="@+id/a2"
    *      android:layout_alignLeft="@+id/a2"
    *      android:layout_alignStart="@+id/a2" />
    *  <Button
    *      android:id="@+id/c2"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="5"
    *      android:layout_below="@+id/b2"
    *      android:layout_alignLeft="@+id/b2"
    *      android:layout_alignStart="@+id/b2" />
    *  <Button
    *      android:id="@+id/d2"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="8"
    *      android:layout_below="@+id/c2"
    *      android:layout_alignLeft="@+id/c2"
    *      android:layout_alignStart="@+id/c2" />
    *  <Button
    *      android:id="@+id/e4"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="="
    *      android:layout_below="@+id/d4"
    *      android:layout_toRightOf="@+id/e3"/>
    *  <Button
    *      android:id="@+id/e3"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="."
    *      android:layout_below="@+id/d3"
    *      android:layout_alignLeft="@+id/d3"
    *      android:layout_alignStart="@+id/d3" />
    *  <Button
    *      android:id="@+id/e2"
    *      android:layout_width="wrap_content"
    *      android:layout_height="wrap_content"
    *      android:text="0"
    *      android:layout_below="@+id/d2"
    *      android:layout_alignLeft="@+id/d2"
    *      android:layout_alignStart="@+id/d2" />
    *  </RelativeLayout>
    *  ![002](image/demo2.jpg)
3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
