# all-permutation-of-a-string
https://www.youtube.com/watch?v=TnZHaH9i6-0&amp;t=1s


import java.util.*;
import java.io.*;

public class HelloWorld{

     public static void main(String []args)
     {
        Scanner sc=new Scanner(System.in);
        String str=sc.next();
        int n=str.length();
        int l=0;
        HelloWorld hw=new HelloWorld();
        
        hw.AllCombination(str,l,n-1);
     }
     static void AllCombination(String str,int l,int r)
     {
         if(l==r)
         {
             System.out.println(str);
         }
         else
         {
             for(int i=l;i<=r;i++)
             {
                 String str1=Swap(str,l,i);
                 AllCombination(str1,l+1,r);
             }
         }
     }
     static String Swap(String str,int i,int j)
     {
         char temp;
         char[] ch=str.toCharArray();
         temp=ch[i];
         ch[i]=ch[j];
         ch[j]=temp;
         
         return String.valueOf(ch);
     }
}
