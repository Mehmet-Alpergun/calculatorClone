# Calculator Class

This JavaScript code defines a `Calculator` class that allows users to perform basic arithmetic calculations. It is designed to work with an HTML page that contains number buttons, operation buttons, an equals button, a clear button, and a delete button.

## Constructor

The `Calculator` class is initialized with two parameters: `previousOperandTextElement` and `secondOperandTextElement`. These parameters represent the elements on the HTML page where the previous and current operands will be displayed. The constructor sets these elements and calls the `clear()` method.

## Methods

1. `clear()`: This method resets the calculator by setting the `previousOperand` and `currentOperand` to empty strings and clearing any stored operation.

2. `delete()`: The `delete()` method removes the last character from the current operand, effectively simulating the backspace key.

3. `appendNumber(number)`: This method appends a number to the current operand. It checks if the number is a decimal point and ensures that only one decimal point can be added.

4. `chooseOperation(operation)`: The `chooseOperation()` method is called when an operation button is clicked. It stores the chosen operation, updates the `previousOperand`, and clears the `currentOperand` in preparation for the next number input.

5. `compute()`: The `compute()` method performs the arithmetic calculation based on the stored operation, the previous operand, and the current operand. It updates the `currentOperand` with the result and resets the operation and previous operand.

6. `getDisplayNumber(number)`: This method formats the number to display it properly with thousand separators and decimal points as needed.

7. `updateDisplay()`: The `updateDisplay()` method is responsible for updating the display of the calculator on the HTML page. It sets the text of the elements for previous and current operands.

## Event Listeners

The code also includes event listeners to respond to button clicks on the HTML page:

- Number buttons (`data-number`): When clicked, the corresponding number is appended to the current operand, and the display is updated.

- Operation buttons (`data-operation`): When clicked, the chosen operation is stored, and the display is updated.

- Equals button (`data-equals`): When clicked, the calculation is performed using the stored operation, and the result is displayed.

- Clear button (`data-all-clear`): When clicked, the calculator is cleared, and the display is updated.

- Delete button (`data-delete`): When clicked, the last character in the current operand is removed, and the display is updated.

# Usage

To use the calculator, you can create an HTML page containing number buttons (with `data-number` attribute), operation buttons (with `data-operation` attribute), equals button (with `data-equals` attribute), clear button (with `data-all-clear` attribute), and delete button (with `data-delete` attribute). The elements representing the previous and current operands should also be defined with appropriate attributes.

Then, link the JavaScript file with the `Calculator` class to the HTML page and create a new instance of the `Calculator` class, passing the elements representing the previous and current operands.
