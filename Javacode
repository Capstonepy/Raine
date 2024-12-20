import java.util.Scanner;

public class MenuProgram {

    // Method to simulate a loading screen
    public static void displayLoadingScreen() {
        System.out.println("\u001b[44;1m=============== Loading ===============\u001b[0m");
        for (int i = 0; i < 3; i++) {
            System.out.print(". ");
            try {
                Thread.sleep(500); // Pause for half a second
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        System.out.println("\n\u001b[42;1m======== Loaded Successfully ========\u001b[0m\n");
    }

    // Method to clear the console
    public static void clearConsole() {
        try {
            if (System.getProperty("os.name").contains("Windows")) {
                new ProcessBuilder("cmd", "/c", "cls").inheritIO().start().waitFor();
            } else {
                System.out.print("\033[H\033[2J");
                System.out.flush();
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int choice;
        String userChoice = "Yes"; // Initialize for the first iteration

        // Display loading screen at the start
        clearConsole();
        displayLoadingScreen();

        do {
            clearConsole();
            System.out.println("\u001b[43;1m====================== Welcome to our Menu ===================\u001b[0m");
            System.out.println("\u001b[31m1 - Calculator\u001b[0m");
            System.out.println("\u001b[32m2 - Area & Perimeter\u001b[0m");
            System.out.println("\u001b[33m3 - Area & Circumference\u001b[0m");
            System.out.println("\u001b[34m4 - Conversion\u001b[0m");
            System.out.println("\u001b[35m5 - Exit\u001b[0m");
            System.out.println("Please choose a number (1-5):");

            choice = scan.nextInt();

            switch (choice) {
                case 1: {
                    clearConsole();
                    System.out.println("\u001b[44;1m============== Welcome to our Calculator ================\u001b[0m");
                    System.out.println("\u001b[31mA. Add\u001b[0m");
                    System.out.println("\u001b[32mB. Subtract\u001b[0m");
                    System.out.println("\u001b[33mC. Multiply\u001b[0m");
                    System.out.println("\u001b[34mD. Divide\u001b[0m");
                    System.out.println("\u001b[35mE. Modulus\u001b[0m");

                    System.out.println("Please pick an operator (A-E):");
                    char operator = scan.next().charAt(0);

                    System.out.println("Enter first number:");
                    int n1 = scan.nextInt();

                    System.out.println("Enter second number:");
                    int n2 = scan.nextInt();

                    double result = 0.0;
                    switch (operator) {
                        case 'A':
                            result = n1 + n2;
                            break;
                        case 'B':
                            result = n1 - n2;
                            break;
                        case 'C':
                            result = n1 * n2;
                            break;
                        case 'D':
                            if (n2 != 0) {
                                result = (double) n1 / n2;
                            } else {
                                System.out.println("\u001b[41mError: Division by zero is not allowed.\u001b[0m");
                            }
                            break;
                        case 'E':
                            result = n1 % n2;
                            break;
                        default:
                            System.out.println("\u001b[41mInvalid operator!\u001b[0m");
                            continue;
                    }
                    System.out.println("\u001b[42;1mResult: " + result + "\u001b[0m");
                    break;
                }

                case 2: {
                    clearConsole();
                    System.out.println("\u001b[42;1m============== Welcome to Area & Perimeter ================\u001b[0m");
                    System.out.println("Enter the length of the rectangle:");
                    int length = scan.nextInt();

                    System.out.println("Enter the breadth of the rectangle:");
                    int breadth = scan.nextInt();

                    int area = length * breadth;
                    int perimeter = 2 * (length + breadth);

                    System.out.println("\u001b[33mArea: " + area + "\u001b[0m");
                    System.out.println("\u001b[34mPerimeter: " + perimeter + "\u001b[0m");
                    break;
                }

                case 3: {
                    clearConsole();
                    System.out.println("\u001b[45;1m============== Welcome to Area & Circumference ================\u001b[0m");
                    System.out.println("Enter the radius of the circle:");
                    float radius = scan.nextFloat();

                    double area = 3.14 * radius * radius;
                    double circumference = 2 * 3.14 * radius;

                    System.out.println("\u001b[33mArea: " + area + "\u001b[0m");
                    System.out.println("\u001b[34mCircumference: " + circumference + "\u001b[0m");
                    break;
                }

                case 4: {
                    clearConsole();
                    System.out.println("\u001b[46;1m============== Welcome to Conversion ================\u001b[0m");
                    System.out.println("Enter distance in centimeters:");
                    double cm = scan.nextDouble();

                    double meters = cm / 100;
                    double millimeters = cm * 10;

                    System.out.println("\u001b[32mDistance in meters: " + meters + " m\u001b[0m");
                    System.out.println("\u001b[32mDistance in millimeters: " + millimeters + " mm\u001b[0m");
                    break;
                }

                case 5:
                    clearConsole();
                    System.out.println("\u001b[42;1mExiting. Thank you!\u001b[0m");
                    System.exit(0);

                default:
                    System.out.println("\u001b[41mInvalid choice. Please try again.\u001b[0m");
            }

            System.out.println("\u001b[43;1mDo you want to try again? (Yes/No):\u001b[0m");
            userChoice = scan.next();
        } while (userChoice.equalsIgnoreCase("Yes"));

        scan.close();
    }
}
