九九乘法表
```java
public class hw1{

     public static void main(String []args){
         for(int i=1;i<10;i++){
            for(int j=1;j<10;j++){
                System.out.print(i +"*"+j+"="+i*j+"\n");
            }
            System.out.print("\n");
        }
     }
}
```
基數*偶數
```java
public class hw2{

     public static void main(String []args){
         for(int i=1;i<10;i+=2){
            for(int j=2;j<10;j+=2){
                System.out.print(i +"*"+j+"="+i*j+"\n");
            }
            System.out.print("\n");
        }
     }
}
```
成績計算
```java
import java.util.Scanner;
public class hw4{
    
     public static void main(String []args){
         Scanner scn = new Scanner(System.in);
         int score=0;
	 System.out.print("請輸入成績:");
         score = scn.nextInt();
         while(score>100 || score<0){
             System.out.print("輸入錯誤，請重新輸入\n");
	     score = scn.nextInt();
         }
         if(score>=60 && score<=100){
             System.out.print("及格");
         }
         else if(score>=50 && score<=59){
             System.out.print("需補考");
         }
         else if(score<50 && score>=0){
             System.out.print("不及格");
         }
     }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_4-1.jpg)

最大最小整數
```java
import java.util.Scanner;
public class hw5{
    public static void main(String []args){
     	Scanner scn = new Scanner(System.in);
        int num=0;
        int i=0;
	System.out.print("請輸入一個整數:");
        num = scn.nextInt();
        for(i=0; i<num; i++) {
            if(i*i<num) {
            } else {
                break;
            }
        }
        System.out.print("最大的整數 m, 滿足 m^2 < num:"+(i-1)+"\n");
        System.out.print("最小的整數 n, 滿足 n^2 > num:"+i+"\n");
    }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_4-2.jpg)

年利率計算
```java
import java.util.Scanner;
public class hw6{
    
      public static void main(String []args) {
        Scanner scn = new Scanner(System.in);
        float n=0;
        float rate=0;
        float years=0;
        System.out.print("請輸入本金:");
        n = scn.nextFloat();
        System.out.print("請輸入年利率:");
        rate = scn.nextFloat();
        System.out.print("請輸入儲蓄多少年:");
        years = scn.nextFloat();
        float sum = n;
        for(int i=0;i<years;i++){
            sum = n*rate/100 +n;
            n = sum;
        }
        System.out.print(n);
    }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_4-3.jpg)
