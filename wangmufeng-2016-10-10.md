#2016-10-10工作日报
====================

1. 工作成果
    * 使用android studio完成界面登录和计算机页面布局
2. 工作内容
    * 界面登录布局
        * <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:weightSum="1">


    <ImageButton
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:srcCompat="@drawable/tupian"
        android:id="@+id/imageButton"
        android:layout_weight="0.07" />

    <CheckedTextView
        android:text="                                        这是一个日报登录系统"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.07" />

    <TextView
        android:text="用户名：_____________________"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/textView4"
        android:layout_weight="0.11" />
    <TextView
        android:text="密码：_____________________ "
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.11" />

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

    <CheckBox
        android:text="记住密码"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <TextView
        android:text="         忘记密码 "
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.11" />
    </LinearLayout>


    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

    <Button
        android:text="登录"
        android:layout_width="136dp"
        android:layout_height="wrap_content" />

    <Button
        android:text="注册"
        android:layout_width="136dp"
        android:layout_height="wrap_content"/>
        <Button
            android:text="忘记密码"
            android:layout_width="136dp"
            android:layout_height="wrap_content" />
    </LinearLayout>


</LinearLayout>
    * 计算机布局
        * <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">


    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.78"
        android:text="Hello" />

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="CE" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="C" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="DELETE" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="/" />


    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="1" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="2" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="3" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="+" />

    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="4" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="5" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="6" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="-" />

    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="7" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="8" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="9" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="*" />

    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="+/-" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="0" />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="." />

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="0.00"
            android:text="=" />

    </LinearLayout>
    * 登录代码
        * <manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.feicuiedu.myandroid">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        <activity android:name=".androidDemo">
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>

                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>

    </application>

</manifest>
        * package com.feicuiedu.myandroid;

import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;

/**
 * Created by Administrator on 2016/10/10.
 */

public class androidDemo extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activnty_main);
    }
}

3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
