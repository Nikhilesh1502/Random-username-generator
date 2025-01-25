import random

# Step 1: Define Adjectives and Nouns
adjectives = ["Cool", "Happy", "Funny", "Smart", "Brave", "Silly", "Clever"]
nouns = ["Tiger", "Dragon", "Unicorn", "Phoenix", "Eagle", "Panda", "Wolf"]

# Step 2: Generate Random Combinations
def generate_username():
    adjective = random.choice(adjectives)
    noun = random.choice(nouns)
    return f"{adjective}{noun}"

# Step 3: Add Customization Options
def customize_username(username, add_numbers=True, add_special_chars=True):
    if add_numbers:
        username += str(random.randint(10, 99))  # Append random number
    if add_special_chars:
        special_chars = "!@#$%^&*"
        username += random.choice(special_chars)  # Append random special character
    return username

# Step 4: Save Usernames to a File
def save_to_file(username, filename="usernames.txt"):
    with open(filename, "a") as file:
        file.write(username + "\n")
    print(f"Username saved to {filename}.")

# Step 5: Interactive User Input
def main():
    print("Welcome to the Random Username Generator!")
    
    while True:
        # Generate a basic username
        username = generate_username()
        
        # Ask the user for customization preferences
        add_numbers = input("Include numbers? (yes/no): ").strip().lower() == "yes"
        add_special_chars = input("Include special characters? (yes/no): ").strip().lower() == "yes"
        
        # Customize the username
        username = customize_username(username, add_numbers, add_special_chars)
        print(f"Generated Username: {username}")
        
        # Save the username
        save = input("Would you like to save this username? (yes/no): ").strip().lower() == "yes"
        if save:
            save_to_file(username)
        
        # Option to generate another username
        another = input("Generate another username? (yes/no): ").strip().lower()
        if another != "yes":
            print("Thank you for using the Random Username Generator!")
            break

if __name__ == "__main__":
    main()
