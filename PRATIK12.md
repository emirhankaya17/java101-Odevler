# Sayıların Toplamını Bulan Program
### Ödev
Java döngüler ile tek bir sayı girilene kadar kullanıcıdan girişleri kabul eden ve girilen değerlerden çift ve 4'ün katları olan sayıları toplayıp ekrana basan programı yazıyoruz.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num,sum=0;
        Scanner sc = new Scanner(System.in);
        //input
        while(true)
        {
            System.out.print("Bir sayı giriniz: ");
            num = sc.nextInt();
            if(num%2 == 1)
            {
                System.out.println("Toplam: "+sum);
                break;
            }
            else
            {
                if(num%4 == 0)
                {
                    sum+=num;
                }
            }
        }

    }

}
```