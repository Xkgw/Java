數字陣列反轉
```java
import java.util.Scanner;
public class java1{

     public static void main(String []args){
        Scanner scn = new Scanner(System.in);
        int a[] = {1,2,3,4,5,6,7,8,9}; 
        int max = 0;
        int max_num = 0;
        int temp = 0;
        for(int i=0;i<9;i++){
            System.out.print(a[i] + " ");
        }
        System.out.print('\n');
        for(int i=0;i<9;i++){
            max = a[i];
            max_num = i;
            for(int j=i+1;j<9;j++){
                if(max < a[j]){
                    max = a[j];
                    max_num = j;
                } 
            }
            temp = a[i];
            a[i] = max;
            a[max_num] = temp;
        }
        for(int i=0;i<9;i++){
            System.out.print(a[i] + " ");
        }
     }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_5-1.jpg)

輸入介於0~20，轉成三角形
```java
import java.util.Scanner;
public class java2_1{
    public static void main(String []args) {
        Scanner scn = new Scanner(System.in);
        int n = 0;

        System.out.print("input n, 0<n<=20:");
        n = scn.nextInt();
        while(n>20 || n<0) {
            System.out.print("input n, 0<n<=20:");
            n = scn.nextInt();
        }
        int matx[][] = new int[n+1][];
        for(int i=0; i<=n; i++) {
            matx[i] = new int[i+1];
            for(int j=0; j<i; j++){
                matx[i][j] = '*';
            }
        }
        for(int i=0; i<=n; i++) {
            for(int j=0; j<i; j++){
                System.out.print((char)matx[i][j] + " ");
            }
            System.out.print("\n");
        }
        System.out.print("\n");
    }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_5-2.jpg)

輸入小於100000的數字，找出在下三角形中的陣列位置
```java
import java.util.Scanner;
public class java2_2{
    public static void main(String []args) {
        Scanner scn = new Scanner(System.in);
        int n = 0;
        int num = 0;
        System.out.print("input n, n<100000:");
        n = scn.nextInt();
        while(n>100000 || n<0) {
            System.out.print("input n, n<100000:");
            n = scn.nextInt();
        }
        int matx[][] = new int[n+1][];
        for(int i=0; i<=n; i++) {
            matx[i] = new int[i+1];
            for(int j=0; j<i; j++){
                matx[i][j] = ++num;
            }
        }
        
        for(int i=0; i<=n; i++) {
            for(int j=0; j<i; j++){
                if(matx[i][j] == n){
                    System.out.println("i :" + --i +" j :" + j);
                    System.exit(0);
                }
            }
        }
    }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_5-3.jpg)

輸入六個數字，找出該數字右邊最大 ex：input arr=[17, 18, 5, 4, 6, 1], output: [18, 6, 6, 6, 1, -1]
```java
import java.util.Scanner;
public class java3{

    public static void main(String []args) {
        Scanner scn = new Scanner(System.in);
        int matx[] = {0,0,0,0,0,0};


        for(int i=0; i<6; i++) {
            System.out.print("input  six num this is "+ (int)(i+1) + ":");
            matx[i] = scn.nextInt();
        }

        for(int i=1; i<6; i++) {
            int max = matx[i];
            for(int j=i+1;j<6;j++){
                if(matx[j]>max) max = matx[j];
            }
            matx[i-1]=max;
        }

        matx[5]=-1;
        for(int i=0; i<6; i++) {
            System.out.print(matx[i] + " ");
        }
    }
}
```
![Image_Text](https://github.com/Xkgw/Java/blob/main/img-storage/java_5-4.jpg)
