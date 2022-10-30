判斷小中大括弧是否正確
```java
import java.util.Scanner;
public class HelloWorld{

     public static void main(String []args){
        Scanner scn = new Scanner(System.in);
        String s;
        int x = 0;
	System.out.print("input brackets: ");
        s = scn.next();
        int tap = 0;
        for(x=0;x<s.length();x++){
            if(s.charAt(x) == '('){
                tap = 0;
                for(int i=x+1;i<s.length();i++){
                    if(s.charAt(i) == ')'){
                        if((i-x)%2==0){
                            System.out.println("false!");
                            System.exit(0);
                        }
                        tap = 1;
                    }
                }
                if(tap == 0){
                    System.out.println("false!");
                    System.exit(0);
                }
            }
            else if(s.charAt(x) == '['){
                tap = 0;
                for(int i=x+1;i<s.length();i++){
                    if(s.charAt(i) == ']'){
                        if((i-x)%2==0){
                            System.out.println("false!");
                            System.exit(0);
                        }
                        tap = 1;
                    }
                }
                if(tap == 0){
                    System.out.println("false!");
                    System.exit(0);
                }
            }
            else if(s.charAt(x) == '{'){
                tap = 0;
                for(int i=x+1;i<s.length();i++){
                    if(s.charAt(i) == '}'){
                        if((i-x)%2==0){
                            System.out.println("false!");
                            System.exit(0);
                        }
                        tap = 1;
                    }
                }
                if(tap == 0){
                    System.out.println("false!");
                    System.exit(0);
                }
            }
        }
        if(tap == 1){
            System.out.println("true!");
        }
     }
}
```

![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_6-1.jpg)

判斷東南西北是否有繞過一圈
```java
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.Scanner;
public class HelloWorld{

     public static void main(String []args){
		Scanner scn = new Scanner(System.in);
		String str1;
		int total=0;
		System.out.print("input path= ");
		str1=scn.next();
		int a[]=new int [str1.length()];
		int b[]=new int []{0};
		int[] c = new int[a.length + b.length];
		int count = 0;
		int t=0;
		for(int i=0;i<a.length;i++)
		{
			if(str1.charAt(i)=='N')
			{
				total += 1;
				a[i]=total;
			}
			else if(str1.charAt(i)=='E')
			{
				total += 10;
				a[i]=total;
			}
			else if(str1.charAt(i)=='S')
			{
				total -= 1;
				a[i]=total;
			}
			else if(str1.charAt(i)=='W')
			{
				total -= 10;
				a[i]=total;
			}
		}
		for (int i = 0; i < b.length; i++)
		{
			c[i] = b[i];
			count++;
		}
		for (int j = 0; j < a.length; j++) 
		{
			c[count++] = a[j];
		}
		for(int i=0;i<c.length;i++)
		{
			for(int j=i+1;j<c.length;j++)
			{
				if(c[i] == c[j])
				{
					System.out.print("output: true");
					t=1;
					System.exit(0);
				}
			}
		}
		if(t==0)
		{
			System.out.print("output: false");
		}
	}
}
```

![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_6-2.jpg)

1~num排列在row行內
```java
import java.util.Scanner;
public class HelloWorld{

     public static void main(String []args){
        Scanner scn = new Scanner(System.in);

        int x = 0, y = 0;
        System.out.print("input num and row:");
        x = scn.nextInt();
        y = scn.nextInt();
          
	System.out.print("\n");
        int row = x/(y);
	
	if(x%row!=0){
		row++;
		if(row*(y-1)<x){
			y++;
		}
		for(int i=0;i<y-1;i++)
            		System.out.printf("%4d ",i+1);
        	System.out.print("\n");
        	for(int i=0;i<y-1;i++)
            		System.out.printf("  == ");
		System.out.print("\n");
	}
	else{
		
		for(int i=0;i<y;i++)
            		System.out.printf("%4d ",i+1);
        	System.out.print("\n");
        	for(int i=0;i<y;i++)
            		System.out.printf("  == ");
		System.out.print("\n");
	}
	for(int i=1;i<=row;i++){
		for(int j=i;j<=x;j+=row){
			System.out.printf("%4d ",j);
		}
		System.out.print("\n");
	}
     }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_6-3.jpg)
