找出回文 121 1331
```java
public class HelloWorld{
     public static void main(String []args){
        int r, sum = 0, a = 0, temp, x;
		for (int i = 11;i < 10000;i++)
		{
			temp = i;
			x = i;
			while (x > 0)
			{
				r = x % 10;
				sum = (sum * 10) + r;
				x = x / 10;
			}
			if (temp == sum)
			{
				System.out.print(temp + " ");
				a++;
				if (a == 10)
				{
					System.out.println();
					a = 0;
				}
			}
			sum = 0;
		}
     }
}
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_7-1.jpg)

找中位數
```java
import java.util.Scanner;
import java.util.ArrayList;
import java.util.*; 
public class HelloWorld{

     public static void main(String []args){
		Scanner scn = new Scanner(System.in);
		ArrayList<Integer> num = new ArrayList<Integer>();
		int x = 0;
		int a = 0;
		while(x!=99999){

		    System.out.print("input num:");
		    x = scn.nextInt();
		    if(x==99999){
		        System.exit(0);
		    }
		    num.add(x);
		    Collections.sort(num);
		    int num_size = num.size();
		    if(num_size % 2 == 1){
    	        	a = num.get((num_size-1)/2);
            	    }else {
    	        	a = (num.get(num_size/2-1) + num.get(num_size/2))/2;
            	    }
		    System.out.println(a);
		}
         
     }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_7-2.jpg)

分區輪流停電(1-17區) num為輪流順序 num=5，1->6->11->16->5...
```java
import java.util.Scanner;
public class HelloWorld {

    public static void main(String []args) {
        Scanner scn = new Scanner(System.in);
        int[] a = new int[18];
        int x = 0,count = 0;
	    System.out.print("input random num:");
        x = scn.nextInt();

        for(int i=1; i<18;) {
            a[i]=1; count++;
            System.out.print(i + " ");
            for(int j=0;j<x;j++){
                i++;
                if(i>17) i = i-17;
                while(a[i]!=0) {
                    i++;
                    if(i>17) i = i-17;
                }
                if(i>17) i = i-17;
            }
            if(count >17) System.exit(0);
        }

    }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_7-3.jpg)
