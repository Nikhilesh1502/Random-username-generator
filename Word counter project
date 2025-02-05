def count_words(text):
    """
    Function to count the number of words in a given text.
    Splits the input text based on spaces and returns the total word count.
    """
    words = text.split()  # Splitting the text into words using default whitespace
    return len(words)  # Returning the number of words


def main():
    """
    Main function to handle user input, process the text, and display the word count.
    It keeps running in a loop until the user decides to exit.
    """
    while True:
        # Prompt the user to enter a sentence or paragraph
        user_input = input("Enter a sentence or paragraph (or type 'exit' to quit): ").strip()
        
        # Check if the user wants to exit
        if user_input.lower() == 'exit':
            print("Exiting program. Goodbye!")
            break  # Exit the loop
        
        # Handle the case where the user provides empty input
        if not user_input:
            print("Error: Input cannot be empty. Please enter some text.")
            continue  # Restart the loop
        
        # Count words in the user input
        word_count = count_words(user_input)

        # Display the word count result
        print(f"Word Count: {word_count}\n")


# Run the main function when the script is executed
if __name__ == "__main__":
    main()
