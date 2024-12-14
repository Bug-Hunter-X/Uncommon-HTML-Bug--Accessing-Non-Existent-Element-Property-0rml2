# Uncommon HTML Bug: Accessing Non-Existent Element Property

This repository demonstrates a subtle bug that can occur in HTML when attempting to access a property of a DOM element that does not exist.  This often results in a silent failure, making it difficult to debug.

## The Bug
The bug lies in `bug.html`. The JavaScript code attempts to access `myDiv.nonExistentProperty`, which does not exist.  This results in undefined being returned, without any explicit error message in many browsers.  However, in stricter environments this might throw an error. 

## The Solution
The solution, `solution.html`, demonstrates a robust approach.  Before accessing the property, we explicitly check if it exists using `myDiv.hasOwnProperty('nonExistentProperty')` to avoid errors.