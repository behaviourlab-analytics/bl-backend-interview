# Task One - Quick Coding Exercise

At BehaviourLab, it's very important that all employees use secure passwords. A password is considered secure only if it meets the following four conditions:

1. It must have between 7 and 25 characters
2. It must contain at least one lowercase letter, at least one uppercase letter, and at least one digit
3. It must not contain any individual character more than three times in succession (e.g. "..bbb.." is weak, "..aa...a." is strong)
4. It must _not_ include any of the common passwords in the provided `common-passwords.txt`. You may convert the `common-passwords.txt` into any format of your choice if necessary.

Given a string called `password`, return the number of steps required to make the password secure. If the password is already secure, return 0.

One step can be any of the following three actions:

- Insert one character to the password,
- Delete one character from the password, or
- Replace one character of the password with another character.

### Example Input & Output

_Example 1_

```
Input: password = "z"
Output: 6
```

_Example 2_

```
Input: password = "aA1"
Output: 4
```

_Example 3_

```
Input: password = "1377C0d3"
Output: 0
```

### Our Expectations

- Please don't spend more than 40-60 mins on this task.
- You must use Python to answer this question.
- We're most interested to see problem solving and your approach.
- Keep it simple, keep it DRY, but don't over complicate or over engineer, comment and test as appropriate.
- Include any assumptions you have made.