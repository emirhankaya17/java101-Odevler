# Recursive ile Fibonacci Serisi Bulan Program
Java'da recursive metotlar ile fibonacci serisi bulan program yapıyoruz.
```java
class Main{

    public static int findFibonacci(int num)
    {
        if(num < 1)
            return 0;
        else if(num <=2)
            return 1;
        else
            return findFibonacci(num-1) + findFibonacci(num - 2);
    }

    public static void main(String[] args) {
        System.out.println(findFibonacci(7));
    }
}
```