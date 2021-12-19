# Mükemmel Sayı Bulan Program
Klavyeden girilen bir sayının mükemmel sayı olup/olmadığını bulan ve sayı mükemmel sayı ise ekrana “mükemmel sayıdır.” değilse “mükemmel sayı değildir.” ifadelerini ekrana yazan programı Java dilinde yazınız.

Mükemmel Sayı Nedir ?
Bir sayının kendisi hariç pozitif tam sayı çarpanları (kalansız bölen sayıların) toplamı kendisine eşit olan sayıya mükemmel sayı denir.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num, sum = 0;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Bir sayı giriniz: ");
        num = sc.nextInt();
        //operation
        int pointer = 1;
        while(pointer<num)
        {
            if(num % pointer == 0)
            {
                sum += pointer;
            }
            pointer++;
        }
        if(num == sum)
            System.out.println(num+" Mükemmel sayıdır");
        else System.out.println(num+" Mükemmel sayı değildir");
    }
}
```