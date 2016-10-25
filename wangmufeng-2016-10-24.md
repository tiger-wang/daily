#2016-10-24工作日报
====================

1. 应完成工作
    * 
2. 未完成工作
    * MainAcitivity
    * DetailActivity
    * ClassInfo
    * SQLiteDabseHandle
    * TableInfo
        * package com.example.sqlitedemo;          
          /**
           * Created by Administrator on 2016/10/25.
           */
          
          public class TableInfo {
          
              private Long _id;
              private String name;
              private String number;
          
              public TableInfo(Long id, String name, String number) {
          
              }
          
              public void set_id(Long _id) {
                  this._id = _id;
              }
          
              public void setName(String name) {
                  this.name = name;
              }
          
              public void setNumber(String number) {
                  this.number = number;
              }
          
              public Long get_id() {
                  return _id;
              }
          
              public String getName() {
                  return name;
              }
          
              public String getNumber() {
                  return number;
              }
          
          }
          
    * ViewAdapter
        * package com.example.sqlitedemo;
          import android.widget.BaseAdapter;
          import java.util.ArrayList;
          import java.util.List;
          
          /**
           * Created by Administrator on 2016/10/25.
           */
          
          public abstract class ViewAdapter<T> extends BaseAdapter {
          
              private List<T>listDate = new ArrayList<T>();
          
              public ViewAdapter(){
              }
          
              @Override
              public int getCount() {
                  return listDate.size();
              }
          
              @Override
              public long getItemId(int position) {
                  return position;
              }
          
              @Override
              public T getItem(int position) {
                  return listDate.get(position);
              }
          
              public List<T> getListDate(){
                  return listDate;
              }
          
              public void setListDate(List<T>listDate){
                  this.listDate = listDate;
              }
          
          
          }

3. 工作内容
4. 未完成原因
5. 遇到问题及解析
