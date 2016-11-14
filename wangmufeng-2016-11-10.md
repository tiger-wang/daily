#2016-11-10工作日报
==================

1. 应完成工作
2. 工作内容
      * package com.example.xuxue;
        import android.content.BroadcastReceiver;
        import android.content.Context;
        import android.content.Intent;
        import android.content.IntentFilter;
        import android.os.Bundle;
        
        import java.net.InterfaceAddress;
        
        public class BatteryChange extends BroadcastReceiver {
        
            private setBatteryText setBattery;
        
            @Override
            public void onReceive(Context context, Intent intent) {
                Bundle bundle = intent.getExtras();
        
                //获取当前电量
                int l = bundle.getInt("level");
                //温度
                int t= bundle.getInt("temperature");
                int tt = (int) (t*0.1);
                //获取总电量（电池的电池容量）
                int s = bundle.getInt("scale");
                setBattery.setTxt(" 剩余电量:"+l+"%"+",总电量:"+s+"。"+"电池的温度："+tt);
        
            }
            public interface setBatteryText{
                void setTxt(String a);
            }
            public void getBatteryText(setBatteryText setBattery  ){
                this.setBattery = setBattery;
            }
        }
      * package com.example.xuxue;
        import android.app.Activity;
        import android.content.Intent;
        import android.content.IntentFilter;
        import android.os.Bundle;
        import android.util.Log;
        import android.widget.TextView;
        /*
        BroadcastReceiver 向 Activity 传值
        //MainActivity实现了setBatteryText接口
        在Activity中调用BatteryChange中的
        getBatteryText(setBatteryText setBattery)方法
        把当前对象传到BatteryChange中
        setBatteryTxt要将数据传给Activity,只要调用 实现接口的Activity中的setTxt
         */    
        public class MainActivity extends Activity implements BatteryChange.setBatteryText {
        
            private TextView text;
        
            @Override
            protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.main_item);
        
                text = (TextView) findViewById(R.id.text3);
                IntentFilter intentFilter = new IntentFilter();
                intentFilter.addAction(Intent.ACTION_BATTERY_CHANGED);
                BatteryChange batteryChange = new BatteryChange();
                //注册广播接收器
                registerReceiver(batteryChange,intentFilter);
                //把当前对象传给BatteryChange
                batteryChange.getBatteryText(this);
        
            }
            public void setTxt(String a){
                if(a!=null){
                    text.setText(a);
                    Log.d("MainActivity",a);
                }
            }
        
        }
3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
