
3個數字比大小_不能用if
```java
import java.util.Scanner;
public class class_hw{
    public static void main(String args[]) {
        Scanner scn=new Scanner(System.in);
        int x1;
        int x2;
        int x3;
        int max;
        int min;
        int mid;

        System.out.print("input three nums:");
        x1 = scn.nextInt();
        x2 = scn.nextInt();
        x3 = scn.nextInt();
        max = (x1>x2)?x1:x2;
        max = (max>x3)?max:x3;
        min = (x1<x2)?x1:x2;
        min = (min<x3)?min:x3;
        mid = x1+x2+x3;
        mid = mid-max-min;
        System.out.print("max:"+max+",mid:"+mid+",min:"+min);
    }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_2-1.jpg)

計算距離
```java
import java.util.Scanner;
public class hw4 {
    public static void main(String args[]) {
        Scanner scn=new Scanner(System.in);
        int x1;
        int y1;
        int a;
        int b;
        int c;


        System.out.print("input x1:");
        x1 = scn.nextInt();
        System.out.print("input y1:");
        y1 = scn.nextInt();
        System.out.print("input line ax+by+c\n");
        System.out.print("input a:");
        a = scn.nextInt();
        System.out.print("input b:");
        b = scn.nextInt();
        System.out.print("input c:");
        c = scn.nextInt();
        
        System.out.print("distance:"+Math.abs(a*x1+b*y1+c)/Math.sqrt(a^2+b^2));
    }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_2-2.jpg)

