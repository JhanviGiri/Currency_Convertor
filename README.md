# Currency_Convertor
import java.util.Scanner;

public class Currency_Converter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Conversion rates 
        double usdToInr = 83.0;  //USD = 83 INR
        double usdToEur = 0.92; // USD = 0.92 EUR
        double usdToGbp = 0.77; // USD = 0.77 GBP

        System.out.println("Currency Converter");
        System.out.println("Choose the conversion type:");
        System.out.println("1. USD to INR");
        System.out.println("2. USD to EUR");
        System.out.println("3. USD to GBP");
        System.out.print("Enter your choice (1-3): ");
        int choice = scanner.nextInt();

        if (choice < 1 || choice > 3) {
            System.out.println("Invalid choice. Please restart the program.");
            return;
        }

        System.out.print("Enter the amount in USD: ");
        double usdAmount = scanner.nextDouble();

        double convertedAmount = 0;
        String currency = "";

        switch (choice) {
            case 1:
                convertedAmount = usdAmount * usdToInr;
                currency = "INR";
                break;
            case 2:
                convertedAmount = usdAmount * usdToEur;
                currency = "EUR";
                break;
            case 3:
                convertedAmount = usdAmount * usdToGbp;
                currency = "GBP";
                break;
        }

        System.out.printf("%.2f USD is equal to %.2f %s%n", usdAmount, convertedAmount, currency);
        scanner.close();
    }
}
