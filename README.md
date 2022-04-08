package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
	/*
	Armstrong numbers
	1634 = 1^4 + 6^4 + 3^4 + 4^4
	371 = 3^3 + 7^3 + 1^3
	 */
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter number: ");
        int number = scan.nextInt();
        int digit =1;
        int sum =0;
        int a = number;
        int tempNumber = number;
        while( a>10){
            a /=10;
            digit++;
        }
        do{
            int b = tempNumber%10;
            tempNumber /=10;
            sum += Math.pow(b,digit);


        } while(tempNumber>0);
        if(sum==number){
            System.out.println("THIS NUMBER IS ARMSTRONG NUMBER");
        }
        else{
            System.out.println("THIS NUMBER IS NOT ARMSTRONG NUMBER");
        }

    }
}
