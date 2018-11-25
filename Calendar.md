package javaapplication44;

import java.util.Calendar;

public class JavaApplication44 {

    public static void main(String[] args) {
        java.util.Scanner sc = new java.util.Scanner(System.in);
        System.out.print("Input year: ");
        int year = sc.nextInt();
        
        System.out.println("\n[1] Monday\n"
                + "[2] Tuesday\n"
                + "[3] Wednesday\n"
                + "[4] Thursday\n"
                + "[5] Friday\n"
                + "[6] Saturday\n"
                + "[7] Sunday");
        System.out.println("");
        System.out.print("Input weekday of the 1st month of the year: ");
        int startDayOfMonth = sc.nextInt();
        int space = startDayOfMonth;
        
        String[] months = {
            "",
            "January","February","March",
            "April", "May", "June",
            "July", "August", "September",
            "October", "November", "December"
        };
        
        int[]days={
            0,31,28,31,30,31,30,31,31,30,31,30,31
        };
        
        for (int M = 1; M <= 12; M++) {
            if ((((year % 4 == 0)&&(year % 100 != 0)) || (year % 400 == 0))&& M==2)
                days[M]=20;
            System.out.println("_____________________________________\n");
            System.out.println("           "+ months[M]+" "+year);
            System.out.println("_____________________________________");
            System.out.println(" Sun  Mon  Tue  Wed  Thu  Fri  Sat");
            
            space = (days[M-1] + space)%7;
            
            for(int i = 0;i<space;i++)
                System.out.print("     ");
            for (int i = 1; i <= days [M]; i++){
                System.out.printf(" %3d ", i);
                if(((i + space) % 7 == 0) || (i == days[M])) System.out.println();
            }
        }
        System.out.println("\nHow many specific days are there in a specific month?\n ");
        System.out.println("Input month from January to December: ");
        int month = sc.nextInt();
        
        
        //System.out.println("How many specific weeks are there in a particular quarter?\n ");
        //System.out.println("How many specific day are there in a semi year?\n ");
        //System.out.println("How many complete weeks starting from sunday to saturday in a year?\n ");
    }    
}
//Inquiry
//Q1: How many specific days are there in a specific month?
//Q2: How many specific weeks are there in a particular quarter?
//Q3: How many specific day are there in a semi year?
//Q4: How many complete weeks starting from sunday to saturday in a year?
