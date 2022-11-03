
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
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_3-1.jpg)

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
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_3-2.jpg)

判斷是否數字是否由小至大 2>5>8
```java
import java.util.Scanner;
public class hw1
{
    public static void main(String args[])
    {
        Scanner scn = new Scanner(System.in);
        int num=0;
        System.out.print("Input(less than 5 digits): ");
        num = scn.nextInt();
        int len;
        int[] n = new int[5];
        for(len=0;num>0;len++)
        {

            n[len]=num%10;
            num/=10;
            if(len>=5)
            {
                System.out.print("input less than 5");
                System.exit(0);
            }
        }
        for(int i=0;i<len-1;i++)
        {
            if(n[i]<n[i+1])
            {
                System.out.print("this digits is not well-ordered number");
                System.exit(0);
            }
        }
        System.out.print("this digits is well-ordered number");
        System.exit(0);
    }
    
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_3-3.jpg)

反轉數字
```java
import java.util.Scanner;
public class aaa{
	public static void main(String args[]){
		Scanner scn = new Scanner(System.in);
		int x,sum=0;
		x = scn.nextInt();
		String to_string;
		to_string = Integer.toString(x);

		for(int i=0;i<to_string.length();i++){
			int to_int = (int)(to_string.charAt(i)) - '0';
			sum += to_int*(Math.pow(10,i));
		}
		System.out.print(sum);
	}
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_3-4.jpg)

進制轉換
```java
import java.util.Scanner;
public class hw3 {
    public static void main(String args[]) {
        Scanner scn = new Scanner(System.in);
        String n;
        int r,k;
        int sum=0;
        System.out.print("Input number n: ");
        n = scn.next();
        System.out.print("Input base r: ");
        r = scn.nextInt();
        System.out.print("Input transform base k: ");
        k = scn.nextInt();
        int len = n.length();
        //base num to 10 (only 2-10)
        if(r<11) {
            for(int i=0; i<len; i++) {
                int x = (int)n.charAt(i)-48;
                if(x>r) {
                    System.out.print("Input error, n must < r");
                    System.exit(0);
                }

                sum += (x)*Math.pow(r, len-i-1);
                System.out.print(sum+"\n");

            }
        }
        //base 11-16
        else {
            for(int i=0; i<len; i++) {
                char ch = Character.toLowerCase(n.charAt(i));
                int x=0;
                if(ch<87) x = (int)ch-48;
                else x = (int)ch-87;
                if(x>r) {
                    System.out.print("Input error, n must < r");
                    System.exit(0);
                }
                sum += (x)*Math.pow(r, len-i-1);
            }

        }


        //10 to k
        System.out.print(r +" to " +k +" ans is: " +Integer.toString(sum,k));
        System.exit(0);
    }
}
```
![image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_3-5.jpg)

