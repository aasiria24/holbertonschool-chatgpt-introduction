Enhancing Code Quality and Efficiency with ChatGPT

📌 Project Overview

This task demonstrates how ChatGPT can be used as a practical tool for debugging code and improving code quality. The provided Python script was intended to calculate the factorial of a number passed as a command-line argument, but it contained a logical error that caused the program to run indefinitely.

The goal of this exercise is to identify the bug, understand its root cause, and apply a correct and efficient fix using AI-assisted reasoning.

🎯 Objective

Use ChatGPT to identify and correct errors in a code sample.

Improve understanding of common logical bugs such as infinite loops.

Verify and test the corrected solution.

🐞 Identified Issue

The original code entered an infinite loop due to a missing update of the loop control variable.

Problematic code snippet:

while n > 1:
    result *= n

Explanation:

The variable n was never decremented inside the loop, so the condition n > 1 always remained true. This caused the program to run indefinitely until manually interrupted.

✅ Solution

The issue was resolved by decrementing n during each iteration of the loop.

Fixed code:

#!/usr/bin/python3
import sys

def factorial(n):
    result = 1
    while n > 1:
        result *= n
        n -= 1
    return result

f = factorial(int(sys.argv[1]))
print(f)

🧪 Testing & Verification

The corrected script was tested using different inputs:

$ ./factorial.py 2
2

$ ./factorial.py 5
120

✔️ The program now terminates correctly.
✔️ The output matches the expected factorial values.

🤖 Role of ChatGPT

ChatGPT was used to:

Analyze the runtime behavior of the script

Identify the logical error causing the infinite loop

Propose a clear and correct fix

Explain the issue and solution in a structured manner

This demonstrates how AI can effectively support debugging tasks and improve developer productivity.

📝 Conclusion

Through this task, we successfully applied AI-assisted debugging to enhance code reliability and correctness. This approach reflects real-world development practices where tools like ChatGPT can accelerate problem-solving and improve overall code quality.


