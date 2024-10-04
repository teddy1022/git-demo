# Lottery Number Generator

## Overview

The **Lottery Number Generator** is a simple web-based application that allows users to generate random lottery numbers while excluding specific numbers if desired. Users can also specify how many sets of lottery numbers they want to generate.

The application is implemented using Java Spring MVC for the backend and JSP for the frontend, with Bootstrap used for styling the UI. This document provides an overview of the features, setup, and usage of the application.

## Features

- **Generate Random Lottery Numbers**: Users can generate random lottery numbers ranging from 1 to 49.
- **Exclude Specific Numbers**: Users can specify numbers to exclude from the generated results.
- **Specify Loop Count**: Users can specify how many sets of lottery numbers they want to generate.
- **Error Handling**: Input validation is implemented to ensure the entered values are in a valid format.

## Requirements

- **Java 11 or above**
- **Spring Boot 2.5+**
- **Maven** for building the project
- **H2 Database** for user account storage (optional)
- **Bootstrap 4** for UI styling

## Setup Instructions

To set up and run the Lottery Number Generator application, follow these steps:

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/your-repo/lottery-number-generator.git
   cd lottery-number-generator
   ```

2. **Build the Project**:
   Use Maven to build the project:

   ```sh
   mvn clean install
   ```

3. **Run the Application**:
   Start the Spring Boot application:

   ```sh
   mvn spring-boot:run
   ```

4. **Access the Application**:
   Open a web browser and navigate to:

   ```
   http://localhost:8080/playground/lottery
   ```

## Usage

1. **Access the Lottery Number Generator Page**:

   - Navigate to the **Lottery Number Generator** page through the main menu.

2. **Input Values**:

   - **Exclude Numbers**: Enter numbers (between 1 and 49) to be excluded from the generated results. Use spaces to separate numbers.
   - **Loop Count**: Specify the number of sets of lottery numbers you wish to generate.

3. **Generate Numbers**:

   - Click on the **Generate** button to see the lottery numbers.
   - If there is an input error (e.g., invalid numbers or loop count), an error message will be displayed with instructions on how to correct the input.

4. **View Results**:

   - After submission, the generated lottery numbers will be displayed on a results page.
   - You can click **Generate Again** to generate more numbers.

## Input Validation

- The **Exclude Numbers** field only accepts integers between 1 and 49. If any value is invalid, an error message will appear.
- The **Loop Count** field must be a positive integer greater than zero.

## Error Messages

- **Invalid Loop Count**: "Loop Count must be a positive integer."
- **Invalid Excluded Number**: "Excluded numbers must be between 1 and 49 and separated by spaces."
- **Non-numeric Input**: Any non-numeric input will trigger an appropriate error message.

## Example Scenarios

- **Scenario 1**: You want to generate 3 sets of lottery numbers, excluding the numbers 3, 7, and 15.
  - **Input**: Exclude Numbers: "3 7 15"; Loop Count: "3"
  - **Output**: Three sets of randomly generated numbers, each excluding the specified numbers.

## Technologies Used

- **Java Spring Boot**: Backend framework for handling requests and generating responses.
- **JSP**: Used for server-side rendering of HTML pages.
- **Bootstrap**: CSS framework for styling the UI.
- **H2 Database**: For optional user account management and login.

## Folder Structure

```
lottery-web/
├── pom.xml
└── src
    ├── main
    │   ├── java
    │   │   └── com
    │   │       └── systex
    │   │           └── controller
    │   │               └── LotteryController.java
    │   │           └── model
    │   │               └── LotteryService.java
    │   └── webapp
    │       ├── index.jsp
    │       └── lottery
    │           ├── main.jsp
    │           └── result.jsp
```

## Future Enhancements

- **User Login**: Add a user authentication system to allow users to save their generated lottery numbers.
- **Historical Data**: Provide users with the ability to view previously generated lottery numbers.
- **API Version**: Create an API version of the application so that other applications can make requests for lottery numbers.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions, feel free to reach out to the development team at [your-email@example.com](mailto:your-email@example.com).
