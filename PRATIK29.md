# Dizideki Tekrar Eden Sayıları Bulan Program
Bir sayı dizisindeki tekrar eden çift sayıları belirten bir program yazınız.
```java
public class Main {

    public static boolean isRepeated(int[] array,int index)
    {
        if(index<0 || index >= array.length)
        {
            System.out.println("Wrong index number");
            return false;
        }
        for (int i = 0; i < array.length ; i++) {
            if(index != i && array[index] == array[i])
            {
                return true;
            }
        }
        return false;
    }

    public static void main(String[] args) {
        //def
        int[] list = new int[]{1,2,9,3,4,4,5,6,6,6,7,8,9,11};
        int[] nums = new int[list.length];
        //operations
        for (int i = 0; i < list.length; i++) {
            if( list[i] % 2 ==0 && isRepeated(list,i))
            {
                nums[i] = list[i];
                if(isRepeated(nums,i))
                    nums[i] = 0;
            }
        }
        System.out.print("Sayılar: ");
        for(int num : nums)
        {
            if(num != 0)
                System.out.print(num+" ");
        }
    }
}
```