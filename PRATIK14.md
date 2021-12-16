# Faktöriyel Hesaplayan Program
### Ödev
N elemanlı bir kümenin elemanları ile oluşturulacak r elemanlı farklı grupların sayısı n’in r’li kombinasyonu olarak adlandırılır. N’in r’li kombinasyonu C(n,r) şeklinde gösterilir.

Java ile kombinasyon hesaplayan program yazınız.

### Kombinasyon formülü
C(n,r) = n! / (r! * (n-r)!)
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int n,r;
        long nFac=1,rFac=1,nMinusRFac=1,sum = 0;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("C(n,r) olacak şekilde sırasıyla n ve r giriniz: \nn: ");
        n = sc.nextInt();
        System.out.print("r: ");
        r = sc.nextInt();
        //operation
        int nMinusR = n-r;
        for (int i = n;i>1; i--) {
            nFac*=n;
            n--;
            if(r!=0)
            {
                rFac*=r;
                r--;
            }
            if(nMinusR!=0)
            {
                nMinusRFac*=nMinusR;
                nMinusR--;
            }

        }
        sum = nFac / (rFac * nMinusRFac);
        System.out.println("Kombinasyon: "+sum);
    }

}
```