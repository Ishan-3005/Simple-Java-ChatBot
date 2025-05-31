# Simple-Java-ChatBot
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner var = new Scanner(System.in);
        System.out.println("Hello! I'm ChatBot. Type 'bye' to exit.\n");

        while (true) {
            System.out.print("You: ");
            String input = var.nextLine().toLowerCase().trim();

            if (input.equals("bye")) {
                System.out.println("ChatBot: Goodbye! Have a nice day!");
                break;
            }

            respond(input);
        }

        var.close();
    }

    public static void respond(String input) {
        if (input.contains("hello") || input.contains("hi")) {
            System.out.println("ChatBot: Hello! How can I help you?");
        } else if (input.contains("how are you") || input.contains("what about you")) {
            System.out.println("ChatBot: I'm just a program, but I'm doing fine!");
        } else if (input.contains("name")) {
            System.out.println("ChatBot: I'm a simple Java chatbot.");
        } else if (input.contains("help")) {
            System.out.println("ChatBot: You can ask me basic questions like 'hello', 'how are you', or 'what is your name'.");
        } else {
            System.out.println("ChatBot: I'm not sure how to respond to that.");
        }
    }
}
