import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        // Create Scanner object to read input from the keyboard
        Scanner input = new Scanner(System.in);

        // Ask for the student's name
        System.out.print("Enter student name: ");
        String studentName = input.nextLine();

        // Ask how many scores will be entered
        System.out.print("Enter number of scores: ");
        int numScores = input.nextInt();

        double total = 0;  // Variable to store the sum of all scores

        // Loop to collect each score
        for (int i = 1; i <= numScores; i++) {
            System.out.print("Enter score #" + i + ": ");
            double score = input.nextDouble();
            total += score; // Add the entered score to the total
        }

        // Calculate average
        double average = total / numScores;
        String grade;

        // Assign letter grade based on average
        if (average >= 90) {
            grade = "A";
        } else if (average >= 80) {
            grade = "B";
        } else if (average >= 70) {
            grade = "C";
        } else if (average >= 60) {
            grade = "D";
        } else {
            grade = "F";
        }

        // Display the final results to the user
        System.out.println("\nStudent: " + studentName);
        System.out.println("Average Score: " + average);
        System.out.println("Final Grade: " + grade);

        // Close scanner to prevent memory leaks
        input.close();
    }
}
