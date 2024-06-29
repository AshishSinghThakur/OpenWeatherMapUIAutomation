# OpenWeatherMap UI Tests

This project contains automated tests for the OpenWeatherMap API using Java, Selenium and TestNG.

## Setup
In order to setup this project you'll need following things installed and configured on your local machine

### Prerequisites

- Java Development Kit (JDK) installed (version 8 or higher)
- Maven
- IDE (e.g., IntelliJ IDEA, Eclipse) with Maven support
- Browsers (Chrome, firefox etc)

### Dependencies

- TestNG: For test execution and assertions
- Selenium: For web interaction
- Allure Report: For reporting
- Apache POI: For reading Excel files

## Running the Tests

1. **Open the project in your IDE:**
   - Open your preferred IDE (e.g., IntelliJ IDEA, Eclipse) and import the project.

2. **Run the tests:**
   - Using IDE:
     - Right-click on `testNG.xml`.
     - Select TestNG Suite.
   - Using Maven (command line):
     ```sh
     mvn clean test
     ```
     or
     ```sh
     mvn -DsuiteXmlFile=testng.xml test
     ```

4. **View Test Results:**
   - Test results can be viewed by serving the Allure report by following the steps below:
     1. Run the tests using `testNG.xml` or Maven command.
     2. Open terminal.
     3. Enter the command:
        ```sh
        rm -rf allure-report
        ```
     4. Enter the command:
        ```sh
        allure generate allure-results --clean -o allure-report
        ```
     5. Enter the command:
        ```sh
        allure open allure-report
        ```

## Troubleshooting

### Dependencies

Ensure that all dependencies specified in `pom.xml` are downloaded and available in your Maven repository. If you are having issues opening the Allure report, try cleaning the `allure-report` folder. Use this command:
```sh
rm -rf <folderName>
```