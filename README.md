# MSLearnTypeScript
- Try code on playground @ https://www.typescriptlang.org/play
# Module02 Lab - Use types in TypeScript
- Exercise 1: Modify existing JavaScript code to have strongly typed variables

Open the file module02.ts and locate Exercise 1.

Modify the code to add types to the variable declarations. The compiled JavaScript code should look the same as the original example when you're done.


- Exercise 2: Modify existing JavaScript code that ensures operational outcomes using strongly typed variables
Locate Exercise 2 in module02.ts.

You can use types to ensure operation outcomes. Run the code as is and then modify it to have strongly typed variables.

Address any errors you find so that the result returned to a is 12.

- Exercise 3: Implement an enum type
Locate Exercise 3 in module02.ts.

Implement an enum type called Season that represents the constants "Fall", "Winter", "Spring", and "Summer".

Update the function so you can pass in the season by referencing an item in the enum, for example Season.Fall, instead of the literal string "Fall".

- Exercise 4: Declare an array type
Locate Exercise 4 in module02.ts.

Declare the array as the type to match the type of the items in the array.



# Module 3 Lab - Use interfaces in TypeScript

In this lab, you'll convert some JavaScript code to strongly typed code using interfaces.

The JavaScript code contains two functions: calculateInterestOnlyLoanPayment, which calculates the payment for an interest only loan, and calculateConventionalLoanPayment, which calculates the payment for a conventional loan. As with most loan calculations, both functions accept principal and interestRate parameters. The difference between them is that the calculateConventionalLoanPayment function accepts a third property, months that the calculateInterestOnlyLoanPayment function does not.

Property	Description
principal	The principal amount of the loan.
interestRate	The annual interest rate of the loan. For example, 5% is specified as 5.
months	The term of the loan specified in months. An interest only loan does not require this property because the number of months is irrelevant (the loan will never be repaid when an interest only payment is made each month.)
In this exercise, you will:

Declare an interface called Loan that defines two properties, principal and interestRate.
Declare an interface called ConventionalLoan that extends Loan, and defines the additional property required for a conventional loan, months.
Update the two functions to implement the new interfaces and strongly type the parameters.

- Exercise 1 - Declare the interfaces
Open the file module03.ts.

Locate TODO: Declare the Loan interface. Declare an interface called Loan that defines two properties, principal and interestRate, each as a number.

Locate TODO: Declare the ConventionalLoan interface. Declare an interface called ConventionalLoan that extends Loan, and defines the additional property required for a conventional loan, months, as a number.


- Exercise 2 - Implement the interfaces
Locate TODO: Update the calculateInterestOnlyLoanPayment function. Replace the two parameters in the calculateInterestOnlyLoanPayment function with an object of type Loan (for example, loanTerms: Loan), and enter the return value of the function as a string.

You'll notice a couple of errors because TypeScript does not recognize the parameters interestRate and principal. Replace the parameter names in the function with properties of the Loan object. (For example, loanTerms.interestRate).

Enter the interest and payment variables in the calculateInterestOnlyLoanPayment function as numbers.

Test the calculateInterestOnlyLoanPayment function to verify that it is working correctly. Remember that you must now pass the parameters to the function in the form of a Loan object.

Locate TODO: Update the calculateConventionalLoanPayment function. Update the calculateConventionalLoanPayment function, this time replacing the three parameters with an object of type ConventionalLoan, and enter the return value of the function as a string. Make any remaining updates to the implementation of the calculateConventionalLoanPayment function.


Test the calculateConventionalLoanPayment function to verify that it is working correctly. Remember that you must now pass the parameters to the function in the form of a ConventionalLoan object.
