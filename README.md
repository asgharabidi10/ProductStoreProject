
Project Name:
PRODUCT STORE – DemoBlaze E-Commerce Website
Introduction:
This project involves automated testing of an e-commerce web application: DemoBlaze
(https://www.demoblaze.com/), which allows users to purchase electronic products like phones, laptops, and monitors. All major functionalities of the website were tested using Selenium WebDriver in C#, following the Page Object Model (POM) design pattern.
________________________________________
Tools & Technologies Used:
•	Programming Language: C#
•	Automation Tool: Selenium WebDriver
•	Design Pattern: Page Object Model (POM)
•	Browser: Chrome
•	Unit Testing Framework: MSTest
•	IDE: Visual Studio
________________________________________
Framework Design – Page Object Model (POM)
The automation framework is structured using the Page Object Model to maintain modular, readable, and reusable code. Below are the key components:
1. BasePage.cs
•	Initializes the Selenium WebDriver and opens the desired URL.
•	Acts as the parent class for all page-specific classes.
2. LoginPage.cs
•	Automates the login functionality.
•	Enters username and password, handles login button and alert.
3. Signup.cs
•	Automates the user signup process.
•	Handles form field entry and submission.
4. Contact.cs
•	Used in the test class to automate the contact form submission.
5. Category.cs
•	Automates category navigation for:
o	Phones
o	Laptops
o	Monitors
6. AddToCart.cs
•	Automates product selection and adding items to the shopping cart.
•	Proceeds through checkout and validates purchase confirmation message.
7. TestClass.cs
•	Contains all functional and negative test cases.
•	Each method uses [TestMethod] attribute from MSTest.
•	Covers all end-to-end workflows.
________________________________________
Test Coverage Summary:
Test Case ID	Feature Tested	Status	Remarks
TC_001	Login (Valid)	Automated	Valid credentials
TC_002	Signup (Valid)	Automated	Valid input fields
TC_003	Contact Form	Automated	Functional test
TC_004-006	Category Views	Automated	Phone, Laptop, Monitor categories
TC_007	Add to Cart	Automated	Adds item to cart
TC_008	Cart & Checkout	Automated	Validates confirmation message
TC_009-014	Negative Scenarios	Automated	Invalid login and signup validations
________________________________________
Test Execution & Results:
Type of Test	Number of Test Cases	Result
Functional Tests	8	Passed
Negative Tests	6	Passed
Total	14	All Passed
________________________________________
Challenges Faced & Solutions:
Challenge	Solution Applied
Static waits causing slowness	Used Thread.Sleep() for timing control
Alert handling after login and cart ops	Managed using driver.SwitchTo().Alert()
Browser closing logic spread in methods	Included driver.Close() within methods
Hardcoded XPath	Used for locating complex elements
________________________________________
Conclusion:
The automated test suite successfully validates the core functionalities of the DemoBlaze e-commerce platform. The use of the Page Object Model ensures clean code architecture and maintainability. This project offers a scalable base for more advanced test scenarios and further test suite expansion

