# Day16-with-java

Today I have practiced and learned how to write a program to print the index of an element present in an array. 

Lets go to the code.....

Here I assumed the number to find out the index is K.

import java.util.Scanner;
public class Day16 {
    static int search(int[] ar, int k)
    {
        for (int i = 0; i < ar.length; i++)
        {
            if (ar[i] == k)
            {
                return i;
            }
        }
        return -1;
    }
    
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for (int i = 0; i < ar.length; i++)
        {
            ar[i] = scan.nextInt();
            
        }
        int k = scan.nextInt();
        int res = search(ar, k);
        System.out.println(res);
        
    }
    
}
out put: 
Array size = 6
Array elements =  1 2 3 4 5 6
k = 4
index of k = 3
 
