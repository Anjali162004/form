# Dynamic Forms Repository

This repository contains three different levels of dynamic forms built using React functional components and hooks. Each level increases in complexity, showcasing different techniques for form handling, validation, conditional logic, and integration with external APIs.

## Table of Contents

1. [Level 1: Basic Dynamic Form with Conditional Fields](#level-1-basic-dynamic-form-with-conditional-fields)
2. [Level 2: Intermediate Dynamic Form with Nested Conditional Logic and Multiple Field Types](#level-2-intermediate-dynamic-form-with-nested-conditional-logic-and-multiple-field-types)
3. [Level 3: Advanced Dynamic Form with Complex Conditional Logic, Dynamic Sections, and Integration with an API](#level-3-advanced-dynamic-form-with-complex-conditional-logic-dynamic-sections-and-integration-with-an-api)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Hosting](#hosting)
7. [License](#license)

## Level 1: Basic Dynamic Form with Conditional Fields

### Objective
Build an event registration form with dynamic fields and simple validation.

### Form Fields
- Name (Text)
- Email (Email)
- Age (Number)
- Are you attending with a guest? (Yes/No)
- Guest Name (Text, visible only if attending with a guest)

### Conditional Logic
- Show the "Guest Name" field only if the "Are you attending with a guest?" field is answered with "Yes".

### Validation
- Name: Required
- Email: Required and must be a valid email format
- Age: Required and must be a number greater than 0
- Guest Name: Required if attending with a guest

### Submission
- On form submission, display a summary of the entered data.

## Level 2: Intermediate Dynamic Form with Nested Conditional Logic and Multiple Field Types

### Objective
Build a job application form with nested conditional fields, multiple field types, and enhanced validation.

### Form Fields
- Full Name (Text)
- Email (Email)
- Phone Number (Number)
- Applying for Position (Dropdown: Developer, Designer, Manager)
- Relevant Experience (Number of years, visible if "Developer" or "Designer" is selected)
- Portfolio URL (Text, visible if "Designer" is selected)
- Management Experience (Text, visible if "Manager" is selected)
- Additional Skills (Multiple checkboxes: JavaScript, CSS, Python, etc.)
- Preferred Interview Time (Date and Time Picker)

### Conditional Logic
- Show "Relevant Experience" if "Developer" or "Designer" is selected.
- Show "Portfolio URL" if "Designer" is selected.
- Show "Management Experience" if "Manager" is selected.

### Validation
- Full Name: Required
- Email: Required and must be a valid email format
- Phone Number: Required and must be a valid number
- Relevant Experience: Required if "Developer" or "Designer" is selected, and must be a number greater than 0
- Portfolio URL: Required if "Designer" is selected, and must be a valid URL
- Management Experience: Required if "Manager" is selected
- Additional Skills: At least one skill must be selected
- Preferred Interview Time: Required and must be a valid date and time

### Submission
- On form submission, display a summary of the entered data.

## Level 3: Advanced Dynamic Form with Complex Conditional Logic, Dynamic Sections, and Integration with an API

### Objective
Build a survey form with complex conditional fields, dynamic sections, and integration with an external API for data fetching.

### Form Fields
- Full Name (Text)
- Email (Email)
- Survey Topic (Dropdown: Technology, Health, Education)
- Technology Section (Visible if "Technology" is selected):
  - Favorite Programming Language (Dropdown: JavaScript, Python, Java, C#)
  - Years of Experience (Number)
- Health Section (Visible if "Health" is selected):
  - Exercise Frequency (Dropdown: Daily, Weekly, Monthly, Rarely)
  - Diet Preference (Dropdown: Vegetarian, Vegan, Non-Vegetarian)
- Education Section (Visible if "Education" is selected):
  - Highest Qualification (Dropdown: High School, Bachelor's, Master's, PhD)
  - Field of Study (Text)
- Feedback (Textarea)

### Conditional Logic
- Show "Technology Section" if "Technology" is selected as the survey topic.
- Show "Health Section" if "Health" is selected as the survey topic.
- Show "Education Section" if "Education" is selected as the survey topic.
- Fetch and display additional questions based on the selected survey topic using an external API.

### Validation
- Full Name: Required
- Email: Required and must be a valid email format
- Survey Topic: Required
- Technology Section Fields: Required if "Technology" is selected, and validate accordingly
- Health Section Fields: Required if "Health" is selected, and validate accordingly
- Education Section Fields: Required if "Education" is selected, and validate accordingly
- Feedback: Required and must be at least 50 characters

### Submission
- On form submission, validate the data, fetch additional questions from an external API based on the survey topic, and display a summary of the entered data along with the additional questions.

## Installation

1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/dynamic-forms.git](https://github.com/Anjali162004/form)
   cd dynamic-forms
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Usage

To run the application locally, use the following command:
```bash
npm start
```

The application will be available at `http://localhost:3000`.
 
