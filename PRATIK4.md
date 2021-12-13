# Dairenin Alanını Hesaplayan Program

## Ödev
Yarıçapı r, merkez açısının ölçüsü 𝛼 olan daire diliminin alanı bulan programı yazınız.

𝜋 sayısını = 3.14 alınız.

Formül : (𝜋 * (r*r) * 𝛼) / 360

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        double r,a,pi=3.14;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sırasıyla dairenin yarıçap ve merkez açısının ölçüsünü giriniz\nr= ");
        r= sc.nextDouble();
        System.out.print("a= ");
        a= sc.nextDouble();
        //operation
        double area = pi*r*r*a / 360;
        //output
        System.out.println("Dairenin alanı "+area);
    }

}
```