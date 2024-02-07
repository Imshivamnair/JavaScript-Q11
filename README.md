# JavaScript-Q11
Write a JavaScript program that uses a try-catch block to catch and handle an 'EvalError' when evaluating an invalid expression.

function evaluate_Expression(exp) {
  try {
    const result = eval(exp);
    console.log('Result:', result);
  } catch (error) {
    if (error instanceof EvalError) {
      console.log('EvalError:', error.message);
    } else {
      console.log('Error:', error.message);
    }
  }
}

// Example:
evaluate_Expression('30 + 30'); // Valid expression
evaluate_Expression('3 +'); // Invalid expression

**Sample Output:**

"Result:"
60
"Error:"
"Unexpected end of input"
