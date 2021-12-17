# Harmonik Sayıları Bulan Program
Java ile girilen sayının harmonik serisini bulan program yazacağız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num;
        double sum = 0;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num = sc.nextInt();
        for (int i = 1; i <= num; i++) {
            sum += (1/(double)i);
        }
        System.out.println("Sonuç: "+sum);
    }
}
```