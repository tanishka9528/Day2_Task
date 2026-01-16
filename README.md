import java.util.Scanner;

public class Calculator {

    // Static variable (shared)
    static String organization = "Elevate Labs";

    // Instance variable
    int instanceValue = 50;

    public static void main(String[] args) {

        // Local variables
        byte b = 10;        // small integer
        short s = 100;
        int a;
        long l = 100000L;
        float f = 10.5f;
        double d;
        char ch;
        boolean status;

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first integer: ");
        a = sc.nextInt();

        System.out.print("Enter second integer: ");
        int b2 = sc.nextInt();

        System.out.print("Enter a decimal number: ");
        d = sc.nextDouble();

        System.out.print("Enter a character: ");
        ch = sc.next().charAt(0);

        System.out.print("Enter true/false: ");
        status = sc.nextBoolean();

        // Arithmetic operations
        int sum = a + b2;
        int diff = a - b2;
        int mul = a * b2;

        // Division with validation
        if (b2 == 0) {
            System.out.println("Division not possible (divide by zero)");
        } else {
            double div = (double) a / b2;
            System.out.printf("Division = %.2f\n", div);
        }

        // Type casting
        int castValue = (int) d;

        // Instance variable access
        Calculator obj = new Calculator();
        System.out.println("Instance Value = " + obj.instanceValue);

        // Output
        System.out.println("Byte = " + b);
        System.out.println("Short = " + s);
        System.out.println("Long = " + l);
        System.out.println("Float = " + f);

        System.out.printf("Sum = %d\n", sum);
        System.out.printf("Difference = %d\n", diff);
        System.out.printf("Multiplication = %d\n", mul);
        System.out.printf("Double to int (type casting) = %d\n", castValue);
        System.out.println("Character = " + ch);
        System.out.println("Boolean = " + status);
        System.out.println("Organization = " + organization);

        sc.close();
    }
}
