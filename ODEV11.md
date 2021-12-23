# Recursive Metotlar ile Üslü Sayı Hesaplama
Java dilinde, taban ve üs değerleri kullanıcıdan alınan üs alma işlemini "Recursive" metot kullanarak yapan programı yazınız.
```java
import java.util.Scanner;

class Main{

    private static int getExp(int base,int exp)
    {
        if(base == 0)
            return 0;
        else if(exp == 0 )
            return 1;
        else if(exp == 1)
            return base;
        else
            return base * getExp(base,exp-1);

    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("Taban değeri giriniz :");
        int base = scan.nextInt();
        System.out.print("Üs değeri giriniz :");
        int exponent = scan.nextInt();
        System.out.println("Sonuç: "+getExp(base,exponent));
    }

}
```