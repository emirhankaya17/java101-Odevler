# Dizideki Elemanların Frekansı
Java dilinde, dizideki elemanların kaç kez tekrar edildiğini yani frekanslarını bulan programı yazınız.
```java
import java.util.ArrayList;
import java.util.List;

public class Main {

    public static String getFrequency(int[] array)
    {
        List tempList = new ArrayList<Integer>();
        String returner = "";
        int counter = 0;
        for (int i = 0; i < array.length; i++) {
            if(!tempList.contains(array[i]))
            {
                for (int j = i+1; j < array.length; j++) {
                    if(array[i] == array[j])
                    {
                        counter++;
                    }
                }
                returner =returner + array[i]+" sayısı "+(counter+1)+" kere tekrar etti.\n";
                counter = 0;
                tempList.add(array[i]);
            }
        }

        return returner;
    }

    public static void main(String[] args) {
        int[] list = new int[]{10, 20, 20, 10, 10, 20, 5, 20};
        System.out.println(getFrequency(list));
    }

}
```