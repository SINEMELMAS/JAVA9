# JAVA9
package lab2;
import java.util.Scanner;
public class simpleScreen {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Please enter the first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Please enter the second number: ");
        double num2 = scanner.nextDouble();

        System.out.println("Select an action:");
        System.out.println("1. Addition");
        System.out.println("2. Subtraction");
        System.out.println("3. Multiplication");
        System.out.println("4. Division");

        System.out.print("Enter the number of action: ");
        int  action= scanner.nextInt();

        double result = 0;

        switch (action) {
            case 1:
                result = num1 + num2;
                System.out.println("Result: " + result);
                break;
            case 2:
                result = num1 - num2;
                System.out.println("Result: " + result);
                break;
            case 3:
                result = num1 * num2;
                System.out.println("Result: " + result);
                break;
            case 4:
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + result);
                } else {
                    System.out.println("Error! Division by zero is not allowed.");
                }
                break;
            default:
                System.out.println("Error! Invalid action number.");
        }

        scanner.close();
    }
}
