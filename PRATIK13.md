# Kuvvetleri Bulan Program
### Ödev
Java döngüler ile girilen sayıya kadar olan 4 ve 5'in kuvvetlerini ekrana yazdıran programı yazıyoruz.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num,sum=0;
        int i=4,j=5;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Bir sayı giriniz: ");
        num = sc.nextInt();
        System.out.println("0");
        while(i<=num)
        {
            System.out.println(i);
            if(j<=num)
                System.out.println(j);
            i*=4;
            j*=5;
        }

    }

}
```