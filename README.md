# oops-project
#electricity bill calculator
import java.util.Scanner;

// Abstract class for the customer
abstract class Customer {
    String name;
    String address;
    long mobileNumber;

    public Customer(String name, String address, long mobileNumber) {
        this.name = name;
        this.address = address;
        this.mobileNumber = mobileNumber;
    }

    // Abstract method to calculate the electricity bill
    public abstract double calculateBill();
}

// Subclass for residential customers
class ResidentialCustomer extends Customer {
    int unitsConsumed;

    public ResidentialCustomer(String name, String address, long mobileNumber, int unitsConsumed) {
        super(name, address, mobileNumber);
        this.unitsConsumed = unitsConsumed;
    }

    
    public double calculateBill() {
        // Implement the calculation logic for residential customers
        double unitPrice = 0.5; // Price per unit
        return unitsConsumed * unitPrice;
    }
}

// Subclass for commercial customers
class CommercialCustomer extends Customer {
    int unitsConsumed;

    public CommercialCustomer(String name, String address, long mobileNumber, int unitsConsumed) {
        super(name, address, mobileNumber);
        this.unitsConsumed = unitsConsumed;
    }

    
    public double calculateBill() {
        // Implement the calculation logic for commercial customers
        double unitPrice = 0.7; // Price per unit
        return unitsConsumed * unitPrice;
    }
}

public class Main {
    public static void main(String args[]) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Electricity Billing System");
        System.out.println("Enter customer details:");

        System.out.print("Name: ");
        String name = scanner.nextLine();

        System.out.print("Address: ");
        String address = scanner.nextLine();

     
