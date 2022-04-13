
Write a program to concatenate StringBuilder & StringBuffer objects.

package javaExamples;
public class concatenation {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		 StringBuilder sb1=new StringBuilder("Sushma");
	     StringBuilder sb2=new StringBuilder("Kumari");
	     StringBuilder s=sb1.append(sb2);
	     System.out.println(s.toString());
	     
	System.out.println("====================================");
	 
	StringBuffer sbf1=new StringBuffer();
	sbf1.append("Hello");
	StringBuffer sbf2=new StringBuffer();
	sbf2.append("World");
	StringBuffer sbf=sbf1.append(sbf2);
	System.out.println(sbf.toString());
			}
}



Write a program to get a substring of a StringBuffer.

package javaExamples;

public class StringBufferSubstring {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		StringBuffer sb = new StringBuffer("stringbuffer");  
        System.out.println("string: "+sb);  
        String subsequence= sb.substring(6);  
        //subsequence from start index 6  
        System.out.println("subsequence from start index 6= "+subsequence);
	}
      }


Write a program to display the length and capacity of String, StringBuilder and StringBuffer.

package javaExamples;

public class CapacityAndLength{

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		String sobj1=new String("Sumedha");
        String sobj2=new String("Saran");
        String res=sobj1 + sobj2; 
        System.out.println(res);
        System.out.println("Length: " + res.length());
        
    System.out.println("====================================");
		
   		 StringBuilder sb1=new StringBuilder("Sushma");
	     StringBuilder sb2=new StringBuilder("Kumari");
	     StringBuilder s=sb1.append(sb2);
	     System.out.println(s.toString());
	     System.out.println("Capacity: " +s.capacity());
	     System.out.println("Length: " + res.length());
	     
	System.out.println("====================================");
	 
	StringBuffer sbf1=new StringBuffer();
	sbf1.append("Hello");
	StringBuffer sbf2=new StringBuffer();
	sbf2.append("World");
	StringBuffer sbf=sbf1.append(sbf2);
	System.out.println(sbf.toString());
	System.out.println("Capacity: " +sbf.capacity());
	System.out.println("Length: " + sbf.length());
	}
      }

Write a program to check whether two given strings contains same set of characters as well as having same length.

input
 String s1 = "amar";
 String s2= "rama";
 
 output : Both contains same characters

package javaExamples;

import java.util.Arrays;

public class SameSetOfCharacaterAndLength {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		String str1 = "amar";                 
		String str2 = "rama";
		char[] chars1 = str1.toCharArray();
		char[] chars2 = str2.toCharArray();
		Arrays.sort(chars1);
		Arrays.sort(chars2);
              if(Arrays.equals(chars1,chars2)) {
		        System.out.println(str1 + " and " + str2 + " have same set of character");
		} else {
		        System.out.println(str1 + " and " + str2 + " not have same set of character");
		}
		
		
		System.out.println("Length of str1: " + str1.length());
		System.out.println("Length of str2: " + str2.length());
		if(str1.length()==str2.length()) {  
            System.out.println(str1 + " and " + str2 + " have same length");  
        }  
    
        if(str2.length()!=str2.length()) {  
            System.out.println(str1 + " and " + str2 + " not have the same length");  
        } 
		
		
	}
 
     }


Write a program to lexicographically arrange the given strings "Raman" , "Aman" , "Vikram" , "Shyam" and "Bhuvan".

public class Main {  
   public static void main(String[] args) {  
      String[] name = { "Raman","Aman","Vikram","Shyam","Bhuvam"};  
      int n = 5;  
      System.out.println("Before Sorting");  
      for(int i = 0; i < n; i++) {  
         System.out.println(name[i]);  
      }  
      for(int i = 0; i < n-1; ++i) {  
         for (int j = i + 1; j < n; ++j) {  
            if (name[i].compareTo(name[j]) > 0) {  
               String temp = name[i];  
               name[i] = name[j];  
               name[j] = temp;  
            }  
         }  
      }  
      System.out.println("\nAfter performing lexicographical order: ");  
      for(int i = 0; i < n; i++) {  
         System.out.println(name[i]);  
      }  
   }  
}  

Wrapper Classes (Integer, Byte, Short, Long, Float, Double, Character, Boolean)
Create objects of all the wrapper classes and print then on console, with using constructor.

package javaExamples;

public class Wrapper {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Integer myInt = 10;
	    Double myDouble = 11.65;
	    Character myChar = 'T';
	    Boolean myBool= true;
	    System.out.println(myInt);
	    System.out.println(myDouble);
	    System.out.println(myChar);
	    System.out.println(myBool);
         }
      }
Write a program to demonstrate boxing and un-boxing.

package javaExamples;

public class BoxingUnboxing {

	public static void main(String[] args) {
		
		//boxing
        Integer objInteger = Integer.valueOf(10);
        //un-boxing
        int a = objInteger.intValue();
       
         System.out.println(a);
	}
   }

Write a program to demonstrate autoboxing and unboxing.

package javaExamples;

public class AutoboxingUnboxing {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//autoboxing
        Integer objInteger = 10;
        //un-boxing
        int a = objInteger;
       System.out.println(a);
	}
     }


Create an array of 5 integers and print sum and average by creating Integer sum(Integer[] arr) and Double average(Integer sum, Integer numberOfElements). Do casting as required for getting proper result.


package javaExamples;

import java.util.Scanner;

public class SumAndAverage {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Integer[] arr = {60, 12, 9, 60, 18};
        SumAndAverage obj = new SumAndAverage();
        Integer sum = obj.sum(arr);
        Integer numberOfElements = arr.length;
        Double ave = obj.average(sum, numberOfElements);
        System.out.println("sum = " + sum);
        System.out.println("average = " + ave);
       
       }

      public Double average(Integer sum, Integer numberOfElements) {
        Double response = 0.0;
        response = (double) sum / numberOfElements;
        return response;
    }
       public Integer sum(Integer[] arr) {
        Integer response = 0;
        for (Integer integer : arr) {
            response += integer;
        }
        return response;
    }
       }

Write a program to print ASCII values of Character objects using wrapper class.


package javaExamples;

public class PrintASCIIValue {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Character obj = Character.valueOf('a');
        System.out.println((int)obj); 
		}  
	}

Create a List of 10 Integer objects and try to access 15th index. Properly analysis the output.

import java.util.ArrayList;

public class AccessIndex {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		ArrayList<Integer> integers = new ArrayList<>();
	     
        integers.add(1);
        integers.add(2);
        integers.add(3);
        integers.add(4);
        integers.add(5);
        integers.add(6);
        integers.add(7);
        integers.add(8);
        integers.add(9);
        integers.add(10);
        //printing the list
        System.out.println("printing list");
        System.out.println(integers);
        int no = integers.get(15);
        System.out.println(no);
    }
  }

