# Asal Sayıları Bulan Program
Java ile 1 - 100 arasındaki asal sayıları ekrana yazdıran programı yazınız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num;
        boolean flag = true;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num = sc.nextInt();
        //operation
        for (int i = 2; i <= num; i++) {

            for (int j = i-1; j > 1; j--) {
                if(i%j == 0)
                {
                    flag = false;
                    break;
                }
            }
            if(flag)
                System.out.print(i+" ");
            flag = true;
        }

    }
}
```