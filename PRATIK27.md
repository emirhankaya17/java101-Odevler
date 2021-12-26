# Dizideki Maksimum ve Minimum Değerleri Bulan Program

Dizideki elemanların girilen sayıdan küçük en yakın sayıyı ve en büyük en yakın sayıyı bulan programı yazınız.
```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        //def
        int[] list = {15,12,788,1,-1,-778,2,0};
        int num,max = Integer.MAX_VALUE,min = Integer.MIN_VALUE;
        Scanner sc = new Scanner(System.in);
        //operation
        System.out.print("Bir sayı giriniz : ");
        num = sc.nextInt();
        for (int i = 0; i <list.length ; i++) {
            if(list[i] > num && list[i]<max )
                max = list[i];
            if(list[i] < num && list[i]>min)
                min = list[i];
        }
        //out
        System.out.println("Girilen sayıdan küçük en yakın sayı : "+min);
        System.out.println("Girilen sayıdan büyük en yakın sayı : "+max);
    }
}
```
