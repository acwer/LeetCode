
## 题目信息
![在这里插入图片描述](https://img-blog.csdnimg.cn/5561c1cb8fe54e0195cf3b43ec3e40d8.png)
## 解题思路

模板题 Acwing第875题(快速幂)
 
 
 ## 相关代码
```
class Solution {
    public double myPow(double x, int n) {
        double s = quick_power(x,n);
        return s;
    }
    public double quick_power(double x,int n){
        int flag=0;
        double s = 1;
        long t = n;
        if(n == 0 || x == 1.0) return 1.0;
        if(n == 1) return x;
        if(n>=0){
           flag=1;
       }
       else{
           t=-t;
       }
        while(t!=0){
             if(t%2==1){
                s=s*x;
                t--;
            }
            x = x*x;
            t = t/2;
        }
        if(flag==1) return s;
        else return 1/s;

    }
}
```
