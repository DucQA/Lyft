# Lyft Automation Test Project

## Overview
This project is an automation testing framework for the Lyft mobile application. It is built using **Java**, **Appium**, and follows the **Page Object Model (POM)** design pattern. The framework is designed to support **data-driven testing** by reading test data from Excel files. The project is managed using **Maven** for dependency management and build automation.

Click the image below to watch a demo of the project in action:

[![Watch the demo](assets/demo.gif)](https://www.youtube.com/watch?v=sWcC1Z_eX_8)

## Features
- Cross-platform support for **Android** and **iOS**.
- **Page Object Model (POM)** for better code maintainability and reusability.
- **Data-driven testing** using Excel files for dynamic test data.
- Integration with **TestNG** for test execution and reporting.
- Configurable via a centralized `ConfigReader` for platform-specific settings.

## Prerequisites
- **Java Development Kit (JDK)** 8 or higher.
- **Maven** installed and configured.
- **Appium Server** installed and running.
- Android/iOS device or emulator/simulator.
- Excel file with test data.

## Project Structure
```
src/
├── main/
│   ├── java/
│   │   ├── Config/               # Configuration reader classes
│   │   ├── Utility/              # Utility classes (e.g., ExcelReader, Platform)
│   │   ├── Pages/                # Page Object Model classes
│   └── resources/                # Resource files (e.g., Excel test data)
├── test/
│   ├── java/                     # Test classes
│   └── resources/                # Test-specific resources
```

## Key Components
### 1. **Page Object Model (POM)**
Each screen of the Lyft app is represented as a separate class under the `Pages` package. These classes encapsulate the locators and actions for the respective screens.

### 2. **Data-Driven Testing**
Test data is stored in Excel files and read using the `ExcelReader` utility. This allows for dynamic and flexible test execution.

### 3. **Platform-Specific Configuration**
The `Platform` utility determines whether the tests are running on Android or iOS. The `ConfigReader` centralizes platform-specific configurations like `platformName`, `deviceId`, and `appiumServerUrl`.

## Dependencies
- **Java**: Programming language for the framework.
- **Appium**: Mobile automation framework.
- **Apache POI**: For reading Excel files.
- **TestNG**: Test execution and reporting.
- **Maven**: Build and dependency management.