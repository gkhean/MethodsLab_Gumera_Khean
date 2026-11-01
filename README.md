# MethodsLab_Gumera_Khean
package com.mycompany.methodslab.java;
import java.util.Scanner;
/**
 *
 * @author dell
 */
public class MethodsLabJava {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        // TASK 1: GREET USER
        System.out.println("TASK 1");
        Printkei();

        // TASK 2: ARITHMETIC METHODS
        System.out.println("\nTASK 2: ARITHMETIC METHODS");

        int num1 = 20;
        int num2 = 5;

        System.out.println("Addition: " + Addition(num1, num2));
        System.out.println("Subtraction: " + Subtraction(num1, num2));
        System.out.println("Multiplication: " + Multiplication(num1, num2));
        System.out.println("Division: " + Division(num1, num2));

        // TASK 3: FACTORIAL
        System.out.println("\nTASK 3: FACTORIAL");

        int factorialResult = Factorial(5);
        System.out.println("Factorial: " + factorialResult);

        // TASK 4: SUM ARRAY
        System.out.println("\nTASK 4: SUM ARRAY");

        int[] numbers = {10, 20, 30, 40, 50};

        System.out.println("Sum: " + sumArray(numbers));

        // TASK 5: PRIME NUMBER
        System.out.println("\nTASK 5: PRIME NUMBER");

        int primeNumber = 7;

        if (isPrime(primeNumber)) {
            System.out.println(primeNumber + " is a prime number.");
        } else {
            System.out.println(primeNumber + " is not a prime number.");
        }

        // ADDITIONAL TASK: MAX IN ARRAY
        System.out.println("\nADDITIONAL TASK: MAX IN ARRAY");

        System.out.println("Maximum: " + maxInArray(numbers));

        input.close();
    }

    // TASK 1: GREET USER
    static void Printkei() {
        System.out.println("Hello Good Morning");
        System.out.println("Welcome to my code");
    }

    // TASK 2: ARITHMETIC METHODS

    static int Addition(int a, int b) {
        return a + b;
    }

    static int Subtraction(int a, int b) {
        return a - b;
    }

    static int Multiplication(int a, int b) {
        return a * b;
    }

    static double Division(double a, double b) {
        if (b == 0) {
            System.out.println("Cannot divide by zero.");
            return 0;
        }

        return a / b;
    }

    // TASK 3: FACTORIAL

    static int Factorial(int n) {

        if (n < 0) {
            return -1;
        }

        int res = 1;

        for (int i = 1; i <= n; i++) {
            res = res * i;
        }

        return res;
    }

    // TASK 4: SUM ARRAY

    static int sumArray(int[] numbers) {

        int sum = 0;

        for (int i = 0; i < numbers.length; i++) {
            sum = sum + numbers[i];
        }

        return sum;
    }

    // TASK 5: PRIME NUMBER

    static boolean isPrime(int n) {

        if (n <= 1) {
            return false;
        }

        for (int i = 2; i < n; i++) {

            if (n % i == 0) {
                return false;
            }
        }

        return true;
    }

    // ADDITIONAL TASK: MAX IN ARRAY

    static int maxInArray(int[] numbers) {

        if (numbers.length == 0) {
            throw new IllegalArgumentException("Array cannot be empty.");
        }

        int max = numbers[0];

        for (int i = 1; i < numbers.length; i++) {

            if (numbers[i] > max) {
                max = numbers[i];
            }
        }

        return max;
    }

    }
