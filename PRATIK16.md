# Basamak Sayılarının Toplamını Hesaplayan Program
### Ödev
Bir sayının basamak sayılarının toplamını hesaplayan program yazınız.

Örnek : 1643 = 1 + 6 + 4 + 3 = 14
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num,sum = 0;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num = sc.nextInt();
        int temp = num;
        while(true)
        {
            if(temp<10)
            {
                sum += temp;
                System.out.println(temp + " = "+sum);
                break;
            }
            System.out.print(temp%10+" + ");
            sum += (temp%10);
            temp/=10;
        }

    }
}
```