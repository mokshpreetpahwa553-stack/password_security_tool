 Password Security Tool

A command line Python application that generates random passwords, analyzes password strength, and provides security recommendations. Built as a beginner learning project to understand password security concepts.

 Features

- Password Generator: Create random passwords of any length
- Strength Checker: Analyze passwords using a 10-point scoring system
- Smart Suggestions: Get recommendations to improve password security
- Combined Mode: Generate and immediately check password strength
- Security Warnings: Detect common passwords, repeated characters, and sequential patterns

### Steps

1. Clone the repository:
```bash
git clone https://github.com/yourusername/password-security-tool.git
cd password-security-tool
```

2. Run the program:
```bash
python password_generator.py
```

No external dependencies required. Uses only Python standard library.

## Usage

Run the program and choose from 5 options:
```
1. Generate password
2. Check password strength
3. Suggestion to make password stronger
4. Generate password and check strength
5. EXIT
```

### Examples

**Generate a Password:**
```
Choose option: 1
How long password do you need: 12
Output: aB9$mK2#pL7x
```

**Check Password Strength:**
```
Choose option: 2
Enter password to check: MyPass123!
Output: 
Score: 7/10
Strength: MEDIUM
```

**Get Improvement Suggestions:**
```
Choose option: 3
Enter password: password123
Output:
> Add Uppercase Letters
> Add more symbols and punctuation marks
> Don't use common passwords
```

## How It Works

### Password Strength Analysis

The tool evaluates passwords based on three categories:

**1. Length Score (0-3 points)**
- 6-8 characters: 1 point
- 9-10 characters: 2 points
- 11+ characters: 3 points

**2. Character Variety (0-4 points)**
- Uppercase letters (A-Z): 1 point
- Lowercase letters (a-z): 1 point
- Numbers (0-9): 1 point
- Symbols (!@#$%): 1 point

**3. Complexity Checks (0-3 points)**
- No repeated triplets (aaa, 111): 1 point
- No sequential patterns (abc, 123): 1 point
- Not a common password: 1 point

### Security Detection

The tool automatically detects:
- Common passwords: "admin", "password"
- Repeated characters: Three or more consecutive identical characters
- Sequential patterns: Consecutive letters or numbers (abc, 123)

## Scoring System

| 0-3   | WEAK     | Easily crackable |
| 4-7   | MEDIUM   | Moderate security |
| 8-10  | STRONG   | Good security |

## Example Output

### Weak Password
```
Input: admin
Output:
  Score: 2/10
  Strength: WEAK
  
Suggestions:
  > Password length should be 10
  > Add Uppercase Letters
  > Add digits
  > Add more symbols and punctuation marks
  > Don't use common passwords(password,admin)
```

### Strong Password
```
Input: Tr0p!c@lSt0rm#2024
Output:
  Score: 10/10
  Strength: STRONG
```


## Future Improvements

- Add GUI interface using Tkinter
- Save generated passwords to encrypted file
- Check passwords against breach databases
- Calculate time-to-crack estimates
- Add password entropy calculations
- Implement clipboard copy functionality
- Create customizable password generation
- Add password strength visualization
- Support for passphrase generation
- Export password reports

 


