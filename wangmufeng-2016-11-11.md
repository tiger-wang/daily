#2016-11-11工作日报
==================

1. 应完成工作
2. 工作内容
      * private List<Map<String, Object>> getData() {

        List<Map<String, Object>> result = new ArrayList<Map<String, Object>>();

        /*List<PackageInfo> listPackage = pm.getInstalledPackages(PackageManager.GET_ACTIVITIES);

        for(PackageInfo packageInfo: listPackage) {


            Map<String ,Object> map = new HashMap<String,Object>();
            map.put("iv",pm.getApplicationIcon(packageInfo.applicationInfo));
            map.put("appName",pm.getApplicationLabel(packageInfo.applicationInfo).toString());
            map.put("packageName",packageInfo.applicationInfo.packageName);
            map.put("versionCode",packageInfo.versionCode+"");
            result.add(map);
        }*/

        List<ActivityManager.RunningAppProcessInfo> appProcessInfos = am.getRunningAppProcesses();

        Log.d("process_test",appProcessInfos.size()+"");
        for (ActivityManager.RunningAppProcessInfo appProcessInfo : appProcessInfos) {
            String packageName = appProcessInfo.processName; // 正在运行程序进程名

            Log.d("packageName",packageName+"");
            int pid = appProcessInfo.pid; // 正在运行程序进程ID
            int importance = appProcessInfo.importance; // 正在运行程序进程级别

            Drawable icon; // 所取数据：运行中程序图标
            String lableName; // 所取数据：运行中程序名称
            long size; // 所取数据：运行中程序所占内存
            Debug.MemoryInfo[] memoryInfos = am.getProcessMemoryInfo(new int[]{pid});
            size = (memoryInfos[0].getTotalPrivateDirty()) * 1024;
            try {
                icon = pm.getApplicationIcon(packageName);
                ApplicationInfo applicationInfo = pm.getApplicationInfo(packageName, 0);
                lableName = pm.getApplicationLabel(applicationInfo).toString();

                Map<String ,Object> map = new HashMap<String,Object>();
                map.put("iv",icon);
                map.put("appName",lableName);
                map.put("packageName",packageName);
                map.put("pid",appProcessInfo.pid);
                map.put("size",size);

                if ((applicationInfo.flags & ApplicationInfo.FLAG_SYSTEM) != 0) {

                    map.put("versionCode","系统进程");
                }
                else {
                    map.put("versionCode","用户进程");
                }
                result.add(map);

            } catch (PackageManager.NameNotFoundException e) {
                e.printStackTrace();
            }


        }

        return result;
    }
// 软件管理
private List<Map<String, Object>> getData() {
      ActivityManager   pm = getPackageManager();
        List<Map<String ,Object>> result = new ArrayList<Map<String,Object>>();

        List<PackageInfo> listPackage = pm.getInstalledPackages(PackageManager.GET_ACTIVITIES);

        for(PackageInfo packageInfo: listPackage) {


            Map<String ,Object> map = new HashMap<String,Object>();
            map.put("iv",pm.getApplicationIcon(packageInfo.applicationInfo));
            map.put("appName",pm.getApplicationLabel(packageInfo.applicationInfo).toString());
            map.put("packageName",packageInfo.applicationInfo.packageName);
            map.put("versionCode",packageInfo.versionCode+"");
            result.add(map);
        }


        return result;
    }
3. 未完成工作
4. 未完成原因
5. 遇到问题及解析
