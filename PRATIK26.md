# Dizideki Elemanların Ortalamasını Hesaplayan Program
Dizideki sayıların harmonik ortalamasını hesaplayan programı yazınız.
```java
public class Main {

    public static double getHarmonicMean(int[] numbers)
    {
        double sum = 0;
        for (int i = 0; i < numbers.length ; ++i) {
            sum+= 1/(double)numbers[i];
        }
        return numbers.length/sum;
    }

    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};
        System.out.println("Harmonik ortalama : "+getHarmonicMean(numbers));
    }
}
```