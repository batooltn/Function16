# Function16
Function16_Team16
import java.util.*;
import java.util.concurrent.ThreadLocalRandom;

class Test
{
  public static void main(String args[])
  {
    int[] Array = { 6, 2, 5, 4, 10, 6, 16, 15, 11 };

    shuffluarray(Array);
    for (int i = 0; i < Array.length; i++)
    {
      System.out.print(Array[i] + " ");
    }
    System.out.println();
  }


  static void shuffluarray(int[] ar)
  {
    
    Random rnd = ThreadLocalRandom.current();
    for (int i = ar.length - 1; i > 0; i--)
    {
      int index = rnd.nextInt(i + 1);
      
      int a = ar[index];
      ar[index] = ar[i];
      ar[i] = a;
    }
  }
}
