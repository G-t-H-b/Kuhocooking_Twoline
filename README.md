#include <iostream>
#include <iomanip>

void printLine(char symbol, int length) {
    for (int i = 0; i < length; i++) {
        std::cout << symbol;
    }
    std::cout << std::endl;
}

void printCenteredText(const std::string& text, int width) {
    int padding = (width - text.length()) / 2;
    std::cout << std::setw(padding + text.length()) << text << std::endl;
}

int main() {
    std::string repositoryName = "Kuhocooking_Twoline";
    int projectVersion = 2;
    std::string hackathonName = "Fevrart Hackathon";
    std::string creationDate = "11th February 2024";

    int boxWidth = 40;
    int titleWidth = boxWidth - 2;

    printLine('=', boxWidth);
    printCenteredText(repositoryName, titleWidth);
    printLine('-', boxWidth);
    std::cout << std::left;
    std::cout << std::setw(20) << "Version:" << std::setw(20) << projectVersion << std::endl;
    std::cout << std::setw(20) << "Created for:" << std::setw(20) << hackathonName << std::endl;
    std::cout << std::setw(20) << "Creation Date:" << std::setw(20) << creationDate << std::endl;
    printLine('-', boxWidth);

    return 0;
}
