# Tam Bölünen Sayıların Ortalamasını Hesaplayan Program
Java döngüler ile 0'dan girilen sayıya kadar olan sayılardan 3 ve 4'e tam bölünen sayıların ortalamasını hesaplayan programı yazınız.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        int num,sum=0,counter=0;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Tavan Sayı Giriniz(inclusive): ");
        num = sc.nextInt();
        //condition
        for (int i = 1; i<=num;++i)
        {
            if(i % 3 == 0 && i % 4 == 0 )
            {
                counter++;
                sum+=i;
            }
        }
        System.out.println("Ortalama: "+sum/counter);
    }
    
}
```