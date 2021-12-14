# Hesap Makinesi

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        double s1,s2,sum;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Birinci sayıyı giriniz: ");
        s1 = sc.nextDouble();
        System.out.print("İkinci sayıyı giriniz: ");
        s2 = sc.nextDouble();

        System.out.print("1->toplama ,2->çıkarma, 3->çarpma, 4->bölme \nSeçiminiz: ");
        int operation = sc.nextInt();
        //operation
        switch(operation) {
            case 1:
                sum = s1+s2;
                System.out.println("sonuç: "+sum);
                break;
            case 2:
                sum = s1-s2;
                System.out.println("sonuç: "+sum);
                break;
            case 3:
                sum = s1*s2;
                System.out.println("sonuç: "+sum);
                break;
            case 4:
                sum = s1/s2;
                System.out.println("sonuç: "+sum);
                break;
            default:
                System.out.println("Belirtilen aralıkta bir seçim yapmadınız");
        }
    }

}
```