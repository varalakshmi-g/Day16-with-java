# Day16-with-java

Today I have practiced and learned below programs . 

Lets go to the code.....

#1st program to print the index of an element present in an array

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

#2 nd program to print the sum of max and sum of min values in an array.

import java.util.Scanner;
public class Day16 {
    static int max(int[] ar)
    {
        int max = Integer.MIN_VALUE;
        for (int i = 0; i < ar.length; i++)
        {
            if (ar[i] > max)
            {
                max = ar[i];
            }
        }
        return max;
    }
    
    static int min(int[] ar)
    {
        int min = Integer.MAX_VALUE;
        for (int i = 0; i < ar.length; i++)
        {
            if (ar[i] < min)
            {
                min = ar[i];
            }
        }
        return min;
    }
    
    static int sum(int[] ar)
    {
        int sum = 0;
        for (int i = 0; i < ar.length; i++)
        {
            sum = sum + ar[i];
            
        }
        return sum;
    }
    
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int[] ar = new int[n];
        for (int i = 0; i < ar.length; i++)
        {
            ar[i] = scan.nextInt();
            
        }
        
        int sum = sum(ar);
        int max = max(ar);
        int min = min(ar);
        
        System.out.println(sum - max);
        System.out.println(sum - min);
        
    }
    
}

out put: 
array size: 6
array elements: 1 4 5 2 7 3
sum of max values: 15
sum of min values: 21


#3 rd program to find the product of N-1 elements in an array

import java.util.Scanner;
public class Day16 {
    
    static int[] productOfN_1(int[] ar)
    {
        int p = 1;
        for (int i = 0; i < ar.length; i++) {
            p = p*ar[i];
        }
        int[] res = new int [ar.length];
        for (int i = 0; i < res.length; i++) 
        {
            res[i] = p/ar[i];
        }
        return res;
        
    }
    
     public static void main(String[] args) {
         Scanner scan = new Scanner(System.in);
         int n = scan.nextInt();
         int[] ar = new int[n];
         for (int i = 0; i < ar.length; i++)
         {
             ar[i] = scan.nextInt();
             
         }
         int[] result = productOfN_1(ar);
         for (int i = 0; i < result.length; i++)
         {
             System.out.print(result[i] + " ");
         }
     }
}
 
out put : 
Array size: 5
Array elements: 1 2 4 5 6
product of n-1: 240 120 60 48 40
