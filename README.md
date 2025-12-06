# Interactive Final Exam Study Guide

A comprehensive, interactive study guide webpage for final exam preparation with quizzes, example problems, study tips, and image support.

## Features

- **Expandable Topic Sections**: Each topic can be expanded/collapsed for easy navigation
- **Key Definitions**: Clickable definition cards that expand to show full content
- **Example Problems**: Problems with toggleable solutions
- **Study Tips**: Organized tips for each topic
- **Image Gallery**: Support for lecture notes and images with lightbox viewing
- **Image Upload**: Upload images directly through the interface
- **Interactive Quizzes**: 
  - Multiple choice questions with immediate feedback
  - Fill-in-the-blank questions with answer checking
  - Score tracking per topic
- **Progress Tracking**: Mark topics as studied and track overall progress
- **Local Storage**: Progress and quiz scores are saved automatically
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Print-Friendly**: Optimized CSS for printing study materials

## How to Add Topics

Open `study_guide.html` and find the `studyData` object. Add your topics to the `topics` array using this structure:

```javascript
{
    id: 'topic-1',                    // Unique identifier
    name: 'Topic Name',               // Display name
    description: 'Brief description',  // Optional description
    color: '#667eea',                 // Optional color (hex code)
    studied: false,                   // Will be managed automatically
    definitions: [                    // Array of definitions
        {
            term: 'Term Name',
            content: 'Definition content here'
        }
    ],
    problems: [                       // Array of example problems
        {
            question: 'Problem question?',
            solution: 'Step-by-step solution'
        }
    ],
    tips: [                           // Array of study tips
        'Tip 1',
        'Tip 2'
    ],
    images: [                         // Array of images
        {
            src: 'images/lecture1.jpg',  // File path or base64 data URL
            caption: 'Optional caption'
        }
    ],
    quizzes: [                        // Array of quiz questions
        {
            type: 'multiple',         // 'multiple' or 'fill'
            question: 'Question text?',
            options: ['Option 1', 'Option 2', 'Option 3', 'Option 4'],  // For multiple choice
            correct: 0,               // Index of correct option (0-based)
            explanation: 'Why this answer is correct'
        },
        {
            type: 'fill',
            question: 'Fill in the blank: The answer is ____.',
            answer: 'correct answer',  // Correct answer text
            explanation: 'Explanation of the answer'
        }
    ]
}
```

## Adding Images

### Method 1: File Paths
1. Create an `images` folder in the same directory as `study_guide.html`
2. Add your image files to the folder
3. Reference them in the topic's `images` array:
   ```javascript
   {
       src: 'images/your-image.jpg',
       caption: 'Description of the image'
   }
   ```

### Method 2: Upload Through Interface
1. Open the study guide in your browser
2. Navigate to the topic section
3. Click the "Click to upload an image" area
4. Select an image file
5. The image will be added automatically (stored as base64)

## Usage

1. Open `study_guide.html` in any modern web browser
2. Click on topic headers to expand/collapse sections
3. Click definition cards to see full definitions
4. Click "Show Solution" to reveal problem solutions
5. Take quizzes by selecting answers or filling in blanks
6. Mark topics as "studied" using the checkbox
7. Track your progress with the progress bar at the top

## Progress Tracking

- Check the "Mark as studied" checkbox for each topic you've completed
- Your progress is automatically saved to browser local storage
- The overall progress bar shows completion percentage
- Quiz scores are tracked and saved per topic

## Tips for Adding Content

1. **Start with structure**: Add the topic name, description, and color first
2. **Add definitions**: List key terms and their definitions
3. **Include problems**: Add example problems with detailed solutions
4. **Provide tips**: Share study strategies and important reminders
5. **Add images**: Include lecture notes, diagrams, or reference materials
6. **Create quizzes**: Test understanding with multiple choice and fill-in-the-blank questions

## Browser Compatibility

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## Notes

- All data is stored locally in your browser (localStorage)
- No internet connection required after initial load
- Images uploaded through the interface are stored as base64 (may increase file size)
- For best performance with many images, use file paths instead of uploads

