# Arrays--To-check-Occurrence-of-element-in-Array
Java code for Occurrence of element in Array
*****Arrays*****
package Arrays;

public class OccurrenceOfElement {

    public static int elementCount(int[] arr, int num){
        int count=0;
        for (int i = 0; i < arr.length; i++) {
            if(num == arr[i]){
                count++;
            }
        }
        return count;
    }
}

package Arrays;

import java.util.Scanner;

public class InputArrays {

    public static int[] Input(int x){

        Scanner input = new Scanner(System.in);
        int[] arr = new int[x];
        for (int i = 0; i < arr.length; i++) {
            arr[i]= input.nextInt();
        }
        return arr;
    }
}


package Arrays;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        System.out.println("Enter size of the Array");
        Scanner input = new Scanner(System.in);
        int size = input.nextInt();
        System.out.println("Enter Elements");
        int[] arr1= InputArrays.Input(size);

        System.out.println("Enter Number for frequency check: ");
        int x = input.nextInt();

        int f= OccurrenceOfElement.elementCount(arr1,x);
        System.out.println("Frequency of "+x+ " is: "+f);
    }
}
