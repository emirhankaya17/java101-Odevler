# EBOB-EKOK Bulan Program
### Ödev
Java ile iki sayının EBOB ve EKOK değerlerini "While Döngüsü" kullanarak yazınız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int ebob = 1,ekok = 1,num1,num2;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("1. Sayıyı giriniz: ");
        num1 = sc.nextInt();
        System.out.print("2. Sayıyı giriniz: ");
        num2 = sc.nextInt();
        //operation
        int pointer = Math.min(num1,num2);
        while (pointer>0)
        {
            if(num1 % pointer == 0 && num2 % pointer == 0)
            {
                ebob = pointer;
                break;
            }
            pointer--;
        }

        pointer = (Math.min(num1,num2)/ebob ) +1;
        while (true)
        {
            if(ebob* pointer % num1 ==0 && ebob* pointer % num2 == 0)
            {
                ekok = ebob * pointer;
                break;
            }
            pointer++;
        }

        //output
        System.out.println("Ebob: "+ebob);
        System.out.println("Ekok: "+ekok);
    }
}
```