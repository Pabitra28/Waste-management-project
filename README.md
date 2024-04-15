# Waste-management-project
// Online Java Compiler
import java.util.Scanner;

public class WasteClassificationSystem {
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter characteristics of waste (e.g., type, material, etc.):");
        String wasteCharacteristics = scanner.nextLine();

        String classification = classifyWaste(wasteCharacteristics);
        System.out.println("The waste is classified as: " + classification);

        scanner.close();
    }

    public static String classifyWaste(String characteristics) {
        // Decision rules for waste classification
        if (characteristics.contains("plastic")) {
            return "Recyclable";
        } else if (characteristics.contains("organic")) {
            return "Organic";
        } else if (characteristics.contains("glass")) {
            return "Recyclable";
        } else {
            return "Non-recyclable";
        }
    }
}
