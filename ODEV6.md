# Girilen Sayılardan Min ve Max Değerleri Bulma
Java ile klavyeden girilen N tane sayma sayısından en büyük ve en küçük sayıları bulan ve bu sayıları ekrana yazan programı yazın.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int N,num,max=0,min = Integer.MAX_VALUE;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Kaç tane sayı gireceksiniz: ");
        N = sc.nextInt();
        //operation
        for (int i = 1; i <= N; i++) {
            System.out.print(i+". Sayıyı giriniz:");
            num = sc.nextInt();

            if(num > max)
                max = num;
            if(num < min)
                min = num;
        }
        System.out.println("En büyük sayı: "+max);
        System.out.println("En küçük sayı: "+min);

    }
}
```