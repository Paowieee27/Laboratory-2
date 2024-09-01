// importing a Scanner to be able to input the height and radius
import java.util.Scanner;

// This is the Base class
class Cylinder {
    double radius;
    double height;
    double area;

    // Method to calculate the surface area of the cylinder
    void area() {
        area = 2 * Math.PI * radius * (radius + height);
        System.out.println("Surface Area of the Cylinder: " + area);
    }

    // Method to get input for radius and height from the user
    void getInput() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the Radius of the Cylinder: ");
        radius = scanner.nextDouble();
        System.out.print("Enter the Height of the Cylinder: ");
        height = scanner.nextDouble();
    }
}

// Derived the class Cylinder : CylinderVol
class CylinderVol extends Cylinder {
    double volume;

    // Method to calculate the volume of the cylinder
    void volume() {
        volume = Math.PI * radius * radius * height;
        System.out.println("Volume of the Cylinder: " + volume);
    }
}

// Main class for output of Area and Volume 
public class Main {
         // Create an object of the derived class
  public static void main(String[] args) {
         CylinderVol cylinderVol = new CylinderVol();

        // Get input for radius and Height
        cylinderVol.getInput();

        // Compute and display the Area
        cylinderVol.area();

        // Compute and display the Volume
        cylinderVol.volume();
    }
}
