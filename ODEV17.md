# Matris Transpozunu Bulma
Java dilinde, çok boyutlu diziler ile oluşturulmuş matrisin transpozunu bulan programı yazınız.
```java
import java.util.Arrays;

public class Main {

    public static int[][] getTranspose(int[][] matris)
    {
        int[][] returnerM = new int[matris[0].length][matris.length];
        for (int i = 0; i < returnerM.length; i++) {
            for (int j = 0; j < returnerM[0].length ; j++) {
                returnerM[i][j] = matris[j][i];
            }
        }
        return returnerM;
    }

    public static void main(String[] args) {
        int[][] matris = new int[][]{{2,3,4},{5,6,4}};
        for(int[] arr: getTranspose(matris))
        {
            System.out.println(Arrays.toString(arr));
        }
    }

}
```