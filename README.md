package com.airsoftware.practice01;

import java.util.Scanner;

public class NameAndAgeRequest {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        Scanner ageInput = new Scanner(System.in);
        String phase;

        System.out.println("Whats your name?");
        String name = input.nextLine();

        System.out.println("How old are you?");
        int age = ageInput.nextInt();

        boolean error = false;

        String a = "Age not valid";

        if(age <= 12 && age > 0) a = "your stage of development is childhood.";
        else if(age >= 13 && age <= 17) a = "your stage of development is adolescence.";
        else if(age >= 18 && age <= 60) a = "your stage of development is adulthood.";
        else if(age >= 61 && age <= 100 && age < 101) a = "your stage of development is the elderly.";
        else error = true;
       
        if(error){
            System.out.println(a);
        } else {
            System.out.println("Hi " + name + ", you are " + age + " years old" + ", and " + a);
        }



    }

}
