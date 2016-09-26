 # 2016-09-26工作日志 #
 ====================
 
 1. 已完成内容
    * java.lang.Math
      public final class Math extends Object
 2. 工作成果
    * abs(arg) : 返回arg绝对值,arg可以是:int,long,float,double.
       * 【举例】 Math.abs(-27.86)            == 27.86
              Math.abs(-100.1234)    ==  100.1234
    * ceil(double arg) : 返回>=arg的最小整数.
       * 【举例】 Math.ceil(30.4)         == 31.0
              Math.ceil(-8.0989)   == -8.0 
    * floor(double arg) : 返回<=arg最大整数.
       * 【举例】 Math.floor(30.4)        == 30.0
              Math.floor(-8.0989)   == -9.0
              max(x,y) : 返回x和y中的最大值. 
              min(x,y) : 返回x和y中的最小值.
    * rint(double arg) : 返回最接近arg的整数值. 返回double
       * 【举例】 Math.rint(30.4)         == 30.0
              Math.rint(30.5)        == 31.0
              Math.rint(30.51)      == 31.0
              Math.rint(-8.0989)   == -8.0
              Math.rint(-8.5)         == -8.0
              Math.rint(-8.5989)   == -9.0
    * round(arg) : 返回最接近arg的整数值.   arg为double时返回long,为float时返回int
       * 【举例】 Math.round(30.1)         == 30
              Math.round(30.5)        == 31
              Math.round(30.51)      == 31
              Math.round(-8.0989)   == -8
              Math.round(-8.5)         == -8
              Math.round(-8.5989)   == -9
    * random() : 返回一个介于0与1之间的伪随机数.大多数情况下适应Random类产生随机数.
       * 【举例】 Math.random()   == 0.83636823562201235
    * statem abs
        * static float abs(float a) 
          返回 float 值的绝对值。
        * static double abs(double a) 
          返回 double 值的绝对值。
        * static int abs(int a) 
           返回 int 值的绝对值。
        * static long abs(long a) 
          返回 long 值的绝对值。
    * arg
        * sqrt(double arg) 
          计算参数的平方根,返回类型为double型 
        * pow(double arg1,bouble arg2) 
          计算arg1为底arg2为指数的幂,返回类型为double型
    * static double acos(double a) 
      返回角的反余弦，范围在 0.0 到 pi 之间。
    * static double asin(double a)   
      返回角的反正弦，范围在 -pi/2 到 pi/2 之间
    * static double atan(double a) 
      返回角的反正切，范围在 -pi/2 到 pi/2 之间。
    * static double atan2(double y, double x) 
      将矩形坐标 (x, y) 转换成极坐标 (r, theta)。
    * static double cbrt(double a) 
      返回 double 值的立方根。
    * static double ceil(double a) 
      返回最小的（最接近负无穷大）double 值，该值大于或等于参数，并且等于某个整数。
    * static double cos(double a) 
      返回角的三角余弦。
    * static double cosh(double x) 
      返回 double 值的双曲线余弦。
    * static double exp(double a) 
      返回欧拉数 e 的 double 次幂的值。
    * static double expm1(double x) 
      返回 ex -1。
    * static double floor(double a) 
      返回最大的（最接近正无穷大）double 值，该值小于或等于参数，并且等于某个整数。
    * static double hypot(double x, double y) 
      返回 sqrt(x2 +y2)，没有中间溢出或下溢。
    * static double IEEEremainder(double f1, double f2) 
      按照 IEEE 754 标准的规定，对两个参数进行余数运算。
    * static double log(double a) 
      返回（底数是 e）double 值的自然对数。
    * static double log10(double a) 
      返回 double 值的底数为 10 的对数。
    * static double log1p(double x) 
      返回参数与 1 的和的自然对数。
    * statem max
        * static double max(double a, double b)  
          返回两个 double 值中较大的一个。
        * static float max(float a, float b) 
          返回两个 float 值中较大的一个。
        * static int max(int a, int b) 
          返回两个 int 值中较大的一个。
        * static long max(long a, long b) 
          返回两个 long 值中较大的一个。
    * statem min
        * static double min(double a, double b) 
          返回两个 double 值中较小的一个。
        * static float min(float a, float b) 
          返回两个 float 值中较小的一个。
        * static int min(int a, int b) 
          返回两个 int 值中较小的一个。
        * static long min(long a, long b) 
          返回两个 long 值中较小的一个。
    * static double pow(double a, double b) 
      返回第一个参数的第二个参数次幂的值。
    * static double random()     
      返回带正号的 double 值，大于或等于 0.0，小于 1.0。
    * static double rint(double a)    
      返回其值最接近参数并且是整数的 double 值。
    * statem round
        * static long round(double a) 
          返回最接近参数的 long。
        * static int round(float a)    
          返回最接近参数的 int。
    * statem signum
        * static double signum(double d) 
          返回参数的符号函数；
          如果参数是零，则返回零；
          如果参数大于零，则返回 1.0；
          如果参数小于零，则返回 -1.0。
        * static float signum(float f)     
          返回参数的符号函数；
          如果参数是零，则返回零；
          如果参数大于零，则返回 1.0；
          如果参数小于零，则返回 -1.0。
    * static double sin(double a) 
      返回角的三角正弦。
    * static double sinh(double x)     
      返回 double 值的双曲线正弦。
    * static double sqrt(double a)      
      返回正确舍入的 double 值的正平方根。
    * static double tan(double a) 
      返回角的三角正切。
    * static double tanh(double x) 
      返回 double 值的双曲线余弦。
    * static double toDegrees(double angrad) 
      将用弧度测量的角转换为近似相等的用度数测量的角。
    * static double toRadians(double angdeg) 
      将用度数测量的角转换为近似相等的用弧度测量的角。
    * statem ulp
        * static double ulp(double d) 
          返回参数的 ulp 大小。
        * static float ulp(float f) 
          返回参数的 ulp 大小。
 3. 未完成工作
    * 无
 4. 未完成原因
    * 无
 5. 遇到的问题及解决方案
    * 无
