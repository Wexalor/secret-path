#include <iostream>
#include <string>

// Function to check the secret path
bool checkSecretPath(const std::string& path) {
    // Define the secret path
    const std::string secretPath = "up, up, down, down, left, right, left, right, B, A";
    
    // Compare the provided path with the secret path
    return path == secretPath;
}

int main() {
    std::string userInput;
    
    // Prompt the user to enter the secret path
    std::cout << "Enter the secret path: ";
    std::getline(std::cin, userInput);
    
    // Check if the entered path is correct
    if (checkSecretPath(userInput)) {
        std::cout << "Access granted. Welcome to the secret area!" << std::endl;
    } else {
        std::cout << "Access denied. Incorrect path." << std::endl;
    }
    
    return 0;
}
