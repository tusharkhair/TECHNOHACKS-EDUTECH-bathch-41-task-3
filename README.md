import java.util.Scanner;

public class QuizGame {
    // Define the quiz questions, choices, and correct answers
    static String[][] questions = {
            {"What is the capital of France?", "A. London", "B. Berlin", "C. Paris", "D. Madrid", "C"},
            {"What is the largest planet in our solar system?", "A. Earth", "B. Jupiter", "C. Saturn", "D. Mars", "B"},
            {"Who wrote 'To Kill a Mockingbird'?", "A. Harper Lee", "B. J.K. Rowling", "C. Jane Austen", "D. Mark Twain", "A"},
            {"What is the smallest prime number?", "A. 0", "B. 1", "C. 2", "D. 3", "C"},
            {"Which element has the chemical symbol 'O'?", "A. Gold", "B. Oxygen", "C. Silver", "D. Hydrogen", "B"}
    };

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int score = 0;

        for (int i = 0; i < questions.length; i++) {
            System.out.println("Question " + (i + 1) + ": " + questions[i][0]);
            for (int j = 1; j <= 4; j++) {
                System.out.println(questions[i][j]);
            }
            System.out.print("Enter the letter of your answer: ");
            String answer = scanner.next().trim().toUpperCase();

            if (answer.equals(questions[i][5])) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Wrong! The correct answer is " + questions[i][5] + ".\n");
            }
        }

        System.out.println("Your final score is " + score + " out of " + questions.length + ".");
        scanner.close();
    }
}
