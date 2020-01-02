# Debugging Guide

## General Debugging Pattern:
1. Recognize that a bug exists
2. Replicate the bug
3. Isolate the source of the bug
4. Identify the cause of the bug
5. Determine a fix for the bug
6. Fix the bug and test

## Detailed Debugging Guide:

1. Recognize that a bug exists
    1. App not working as expected?
        1. What did you expect to occur?
        2. What actually happened?
        3. Is there an error in the console/terminal?
            * What does the error say?
            * Do you understand the error?
2. Replicate the bug
    1. When does your app stop working as expected?
        * Doesn’t compile?
        * When you navigate to another route?
        * On click/change/hover/etc?
3. Isolate the source of the bug
    1. Error in the console/terminal?
        1. Does the error tell you what file?
            * Does the error tell you what line in the file?
        2. No file or line number in error?
            * Hypothesize where the bug could be coming from
                * Example: When I click the button, I know that the ‘handleClick’ method should be getting called. I’ll start looking there.
        3. Don’t understand the error?
            * Copy the error and drop it in a Google search
                * Dig through some articles and see what you can find. There is a good chance that someone has run into the same error before
        4. Use the Chrome/VS Code debugger
            * Sources/elements/network/console tabs
                * Use them!
                    * Breakpoints for the win!
    2. No error in the console/terminal?
        1. Hypothesize where the bug could be coming from
            * Example: When I click the button, I know that the ‘handleClick’ method should be getting called. I’ll start looking there.
        2. Use the Chrome/VS Code debugger
            * Sources/elements/network/console tabs
                * Use them!
                    * Breakpoints for the win!
4. Identify the cause of the bug
    1. When the bug is found, identify _why_ it occurred. 
5. Determine a fix for the bug
6. Fix the bug and test
    1. After you have fixed a bug, you need test your application to make sure that you actually solved your problem
        1. What if you fixed a bug in your app, but it wasn’t the bug that was throwing the error? Verify that your app is working as you expect it to.
        2. Go back to step 2 and try to replicate the bug
            * If bug still exists, repeat steps 3 - 6.
