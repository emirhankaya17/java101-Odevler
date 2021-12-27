# Dizideki Elemanları Sıralama
Java dilinde, dizideki elemanları küçükten büyüğe sıralayan programı yazınız. Dizinin boyutunu ve dizinin elemanlarını kullanıcıdan alınız.
```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int size;
        int [] list;
        //op
        System.out.print("Dizinin boyutu: ");
        size = sc.nextInt();
        list = new int[size];

        for (int i = 0; i < list.length; i++) {
            System.out.print((i+1)+". Elemanı : ");
            list[i] = sc.nextInt();
        }
        Arrays.sort(list);
        System.out.println("Sıralama: "+Arrays.toString(list));
    }
    
}
```