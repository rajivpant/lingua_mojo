# Lingua Mojo - v0.1

---

## Project Overview

**Lingua Mojo** is an AI-Enhanced Language Learning Tool designed to provide users with personalized learning paths and interactive exercises. This initial version aims to deliver a functional and innovative language learning experience using modern large language models.

By Rajiv Pant <https://rajiv.com>

---

## Requirements and Features

### Core Features

1. **User Proficiency Assessment**
   - Conduct an initial assessment of the user's language proficiency using a language model.
   - Provide a proficiency level (e.g., Beginner, Intermediate, Advanced).

2. **Personalized Learning Paths**
   - Generate personalized lesson plans based on the user's proficiency level.

3. **Grammar and Vocabulary Exercises**
   - Offer interactive exercises for grammar and vocabulary improvement.
   - Include multiple-choice questions and fill-in-the-blanks exercises.

### Detailed Feature Description

#### 1. User Proficiency Assessment

- **Functionality**:
  - Users will input a sample text in the language they are learning.
  - The app will use a language model to assess the input and determine the user's proficiency level.
- **Output**:
  - A proficiency level categorization (e.g., Beginner, Intermediate, Advanced).

#### 2. Personalized Learning Paths

- **Functionality**:
  - Based on the assessed proficiency level, the app will generate a personalized learning path.
  - The learning path will include lessons tailored to the user's current level.
- **Output**:
  - A list of lessons appropriate for the user's proficiency level.

#### 3. Grammar and Vocabulary Exercises

- **Functionality**:
  - Provide grammar exercises tailored to the user's proficiency level.
  - Provide vocabulary exercises that enhance the user's language skills.
- **Output**:
  - Interactive grammar and vocabulary exercises.

---

## Technical Specifications

### Technology Stack

- **Programming Language**: Mojo
- **External APIs**: OpenAI GPT-4 (or similar language model API)
- **Environment Management**: `.env` file for API keys and environment variables

### Project Structure

```plaintext
lingua_mojo/
│
├── src/
│   ├── main.mojo
│   ├── proficiency_assessment.mojo
│   ├── learning_paths.mojo
│   └── exercises.mojo
│
├── .env
├── .gitignore
└── README.md
```

### Example Code Outline

#### `main.mojo`

```mojo
fn main():
    print("Please enter a sample of your language proficiency:")
    var user_input = ""
    input_line(user_input)
    
    var assessment = initial_assessment(user_input)
    print("Your proficiency level is: ", assessment)
    
    var learning_path = generate_learning_path(assessment)
    print("Your personalized learning path:")
    for lesson in learning_path:
        print(lesson)
    
    var grammar_exercise = generate_grammar_exercise(assessment)
    print("Grammar Exercise: ", grammar_exercise)
    
    var vocabulary_exercise = generate_vocabulary_exercise(assessment)
    print("Vocabulary Exercise: ", vocabulary_exercise)

main()
```

#### `proficiency_assessment.mojo`

```mojo
fn initial_assessment(user_input: str) -> str:
    // Simulate the assessment logic
    if user_input.len() < 50:
        return "Beginner"
    elif user_input.len() < 100:
        return "Intermediate"
    else:
        return "Advanced"
```

#### `learning_paths.mojo`

```mojo
fn generate_learning_path(proficiency: str) -> List[str]:
    if proficiency == "Beginner":
        return ["Lesson 1: Basic Greetings", "Lesson 2: Common Phrases"]
    elif proficiency == "Intermediate":
        return ["Lesson 1: Conversational Practice", "Lesson 2: Intermediate Grammar"]
    else:
        return ["Lesson 1: Advanced Vocabulary", "Lesson 2: Complex Sentences"]
```

#### `exercises.mojo`

```mojo
fn generate_grammar_exercise(proficiency: str) -> str:
    if proficiency == "Beginner":
        return "Fill in the blank: I ___ a student. (am/is/are)"
    elif proficiency == "Intermediate":
        return "Correct the sentence: She don't like apples."
    else:
        return "Rewrite the sentence: He is reading a book in more complex form."

fn generate_vocabulary_exercise(proficiency: str) -> str:
    if proficiency == "Beginner":
        return "Translate to English: Hola (Hello)"
    elif proficiency == "Intermediate":
        return "Provide a synonym for 'happy'."
    else:
        return "Use 'ubiquitous' in a sentence."
```

---

## Environment Setup

### Environment Variables

- **.env File**:

```plaintext
  OPENAI_API_KEY=your_openai_api_key
```

### Git Ignore

- **.gitignore File**:

```gitignore
# Ignore Mac system files
.DS_Store

# Ignore VS Code settings
.vscode/

# Ignore build artifacts
/build/

# Envrionment variables
.env

# Ignore Python cache
__pycache__/
*.pyc
```

---

## Running the Application

1. **Install Mojo**: Ensure Mojo is installed and properly configured.
2. **Navigate to the Project Directory**:

```sh
   cd /path/to/lingua_mojo
```

3. **Run the Application**:

```sh
   mojo run src/main.mojo
```

---

