import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        System.out.println("\n1. Reverse String");
        System.out.println("2. Check Palindrome");
        System.out.println("3. Both");
        System.out.print("Enter your choice: ");
        int choice = sc.nextInt();

        String reverse = "";

        // Reverse the string
        for (int i = str.length() - 1; i >= 0; i--) {
            reverse = reverse + str.charAt(i);
        }

        if (choice == 1) {
            System.out.println("Reversed string: " + reverse);
        }

        else if (choice == 2) {
            if (str.equalsIgnoreCase(reverse)) {
                System.out.println("It is a Palindrome");
            } else {
                System.out.println("It is not a Palindrome");
            }
        }

        else if (choice == 3) {
            System.out.println("Reversed string: " + reverse);

            if (str.equalsIgnoreCase(reverse)) {
                System.out.println("It is a Palindrome");
            } else {
                System.out.println("It is not a Palindrome");
            }
        }

        else {
            System.out.println("Invalid choice");
        }
    }
}
