# Üçgenin Alanını Hesaplayan Program

## Ödev
Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan programı yazınız.

Formül
Üç𝑔𝑒𝑛𝑖𝑛 ç𝑒𝑣𝑟𝑒𝑠𝑖 = 2𝑢

𝑢 = (a+b+c) / 2

Alan * Alan = 𝑢 * (𝑢 − 𝑎)* (𝑢 − 𝑏) * (𝑢 − 𝑐)
```java
import java.util.Scanner;
import java.lang.Math;

public class Main {
    public static void main(String[] args) {
        //def
        double e1,e2,e3;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Üçgenin kenarlarını sırası ile yazın \na= ");
        e1 = sc.nextDouble();
        System.out.print("b= ");
        e2 = sc.nextDouble();
        System.out.print("c= ");
        e3 = sc.nextDouble();
        //operation
        double u = (e1+e2+e3)/2;
        double area = Math.sqrt(u * (u - e1)* (u - e2) * (u - e3));
        //output
        System.out.println("Üçgenin alanı: "+area);

    }

}
```