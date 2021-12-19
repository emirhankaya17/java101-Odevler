# Fibonacci Serisi
Java döngüler ile fibonacci serisi bulan program yazıyoruz. Fibonacci serisinin eleman sayısını kullanıcıdan alın.

Fibonacci Serisi Nedir ?
Fibonacci serisi, her sayının kendinden önceki ile toplanması sonucu oluşan bir sayı dizisidir. Bu şekilde devam eden bu dizide sayılar birbirleriyle oranlandığında altın oran ortaya çıkar, yani bir sayı kendisinden önceki sayıya bölündüğünde altın orana gittikçe yaklaşan bir dizi elde edilir.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num,prev=1,next=1;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num = sc.nextInt();

        System.out.print("1 1 ");
        //operation
        int temp;
        for (int i = 0; i < num-2; i++) {
            temp = next;
            next = next + prev;
            System.out.print(next+" ");
            prev = temp;
        }

    }
}
```