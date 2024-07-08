import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        System.out.print("Enter how many subjects are there: ");
        int numSubjects = scanner.nextInt();


        int[] marks = new int[numSubjects];


        for (int i = 0; i < numSubjects; i++) {
            System.out.print("Enter marks for subject " + (i + 1) + ": ");
            marks[i] = scanner.nextInt();
        }


        int totalMarks = 0;
        for (int mark : marks) {
            totalMarks += mark;
        }

        // Calculate Average Percentage: Divide the total marks by the total number of subjects to get the average percentage
        double averagePercentage = (double) totalMarks / numSubjects;

        // Grade Calculation: Assign grades based on the average percentage achieved
        char grade;
        if (averagePercentage >= 95) {
            grade = 'A';
        } else if (averagePercentage >= 90) {
            grade = 'B';
        } else if (averagePercentage >= 80) {
            grade = 'C';
        } else if (averagePercentage >= 70) {
            grade = 'D';
        } else {
            grade = 'E';
        }

        // Display Results: Show the total marks, average percentage, and the corresponding grade to the user
        System.out.println("Total Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
