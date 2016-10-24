#2016-10-19工作日报
===================

1. 已完成工作
      * 在android studio中使用纯Java编写计算器
2. 工作内容
      * package com.feicuiedu.mydemo5;
        import android.annotation.TargetApi;
        import android.graphics.Color;
        import android.os.Bundle;
        import android.support.annotation.Nullable;
        import android.support.v7.app.AppCompatActivity;
        import android.view.Gravity;
        import android.view.View;
        import android.view.ViewGroup;
        import android.widget.Button;
        import android.widget.EditText;
        import android.widget.GridLayout;
        import android.widget.RelativeLayout;
        
        /**
         * Created by Administrator on 2016/10/20.
         */
        
        public class demo extends AppCompatActivity {
        
        
            @TargetApi(value = 17)
        
            @Override
            protected void onCreate(@Nullable Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                //定义一个相对布局
                RelativeLayout rl = new RelativeLayout(this);
                //给这个布局设定宽和高
                ViewGroup.LayoutParams vp = new ViewGroup.LayoutParams(
                        ViewGroup.LayoutParams.MATCH_PARENT,
                        ViewGroup.LayoutParams.MATCH_PARENT
                );
                //这个布局的宽和高
                rl.setLayoutParams(vp);
                //这个布局的颜色
                rl.setBackgroundColor(Color.BLUE);
        
                //定义一个EditText控件
                EditText et = new EditText(this);
                //给这个控件设置宽和高
                RelativeLayout.LayoutParams etParams = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.MATCH_PARENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                //这个控件的宽和高
                et.setLayoutParams(etParams);
                et.setGravity(Gravity.RIGHT);
                //这个控件的ID
                et.setId(R.id.my_id);
        
                rl.addView(et);
                //设置这个控件的宽和高
                RelativeLayout.LayoutParams btu7Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                //这个控件在et.getId()这个控件下面
                btu7Params.addRule(RelativeLayout.BELOW,et.getId());
                //定义一个Button控件
                Button btu7 = new Button(this);
                //这个控件的宽和高
                btu7.setLayoutParams(btu7Params);
                //这个控件的ID
                btu7.setId(View.generateViewId());
                //这个控件显示的名称
                btu7.setText("7");
                //设置这个控件的宽和高
                RelativeLayout.LayoutParams btu8Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu8Params.addRule(RelativeLayout.BELOW,et.getId());
                btu8Params.addRule(RelativeLayout.RIGHT_OF,btu7.getId());
        
                Button btu8 = new Button(this);
                btu8.setLayoutParams(btu8Params);
                btu8.setId(View.generateViewId());
                btu8.setText("8");
        
                RelativeLayout.LayoutParams btu9Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu9Params.addRule(RelativeLayout.BELOW,et.getId());
                btu9Params.addRule(RelativeLayout.RIGHT_OF,btu8.getId());
        
                Button btu9 = new Button(this);
                btu9.setLayoutParams(btu9Params);
                btu9.setId(View.generateViewId());
                btu9.setText("9");
        
                RelativeLayout.LayoutParams btnParamsMul = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btnParamsMul.addRule(RelativeLayout.BELOW,et.getId());
                btnParamsMul.addRule(RelativeLayout.RIGHT_OF, btu9.getId());
        
                Button btnMul = new Button(this);
                btnMul.setLayoutParams(btnParamsMul);
                btnMul.setId(View.generateViewId());
                btnMul.setText("*");
        
                RelativeLayout.LayoutParams btu4Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu4Params.addRule(RelativeLayout.BELOW,btu7.getId());
        
                Button btu4 = new Button(this);
                btu4.setLayoutParams(btu4Params);
                btu4.setId(View.generateViewId());
                btu4.setText("4");
        
                RelativeLayout.LayoutParams btu5Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu5Params.addRule(RelativeLayout.BELOW,btu8.getId());
                btu5Params.addRule(RelativeLayout.RIGHT_OF,btu4.getId());
        
                Button btu5 = new Button(this);
                btu5.setLayoutParams(btu5Params);
                btu5.setId(View.generateViewId());
                btu5.setText("5");
        
                RelativeLayout.LayoutParams btu6Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu6Params.addRule(RelativeLayout.BELOW,btu9.getId());
                btu6Params.addRule(RelativeLayout.RIGHT_OF,btu5.getId());
        
                Button btu6 = new Button(this);
                btu6.setLayoutParams(btu6Params);
                btu6.setId(View.generateViewId());
                btu6.setText("6");
        
                RelativeLayout.LayoutParams btnParamsMul1 = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btnParamsMul1.addRule(RelativeLayout.BELOW,btnMul.getId());
                btnParamsMul1.addRule(RelativeLayout.RIGHT_OF, btu6.getId());
        
                Button btnMul1 = new Button(this);
                btnMul1.setLayoutParams(btnParamsMul1);
                btnMul1.setId(View.generateViewId());
                btnMul1.setText("/");
        
                RelativeLayout.LayoutParams btu1Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu1Params.addRule(RelativeLayout.BELOW,btu4.getId());
        
                Button btu1 = new Button(this);
                btu1.setLayoutParams(btu1Params);
                btu1.setId(View.generateViewId());
                btu1.setText("1");
        
                RelativeLayout.LayoutParams btu2Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu2Params.addRule(RelativeLayout.BELOW,btu5.getId());
                btu2Params.addRule(RelativeLayout.RIGHT_OF,btu1.getId());
        
                Button btu2 = new Button(this);
                btu2.setLayoutParams(btu2Params);
                btu2.setId(View.generateViewId());
                btu2.setText("2");
        
                RelativeLayout.LayoutParams btu3Params = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btu3Params.addRule(RelativeLayout.BELOW,btu6.getId());
                btu3Params.addRule(RelativeLayout.RIGHT_OF,btu2.getId());
        
                Button btu3 = new Button(this);
                btu3.setLayoutParams(btu3Params);
                btu3.setId(View.generateViewId());
                btu3.setText("3");
        
                RelativeLayout.LayoutParams btnParamsMul2 = new RelativeLayout.LayoutParams(
                        RelativeLayout.LayoutParams.WRAP_CONTENT,
                        RelativeLayout.LayoutParams.WRAP_CONTENT
                );
                btnParamsMul2.addRule(RelativeLayout.BELOW,btnMul1.getId());
                btnParamsMul2.addRule(RelativeLayout.RIGHT_OF, btu3.getId());
        
                Button btnMul2 = new Button(this);
                btnMul2.setLayoutParams(btnParamsMul2);
                btnMul2.setId(View.generateViewId());
                btnMul2.setText("-");
        
                rl.addView(btu1);
                rl.addView(btu2);
                rl.addView(btu3);
                rl.addView(btu4);
                rl.addView(btu5);
                rl.addView(btu6);
                rl.addView(btu7);
                rl.addView(btu8);
                rl.addView(btu9);
                rl.addView(btnMul);
                rl.addView(btnMul1);
                rl.addView(btnMul2);
        
                setContentView(rl);
        
                //setContentView(R.layout.main_demo);
            }
        }

3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
