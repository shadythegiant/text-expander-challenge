

# Text Expander Component

This project is a React component called `TextExpander`, created as part of a React course exercise to explore the concepts of **state** and **props**. The component allows users to expand or collapse a block of text, showing a customizable portion of the content by default and revealing the full text when clicked.

## Purpose
The goal of this exercise is to:
- Understand how to manage component state using the `useState` hook.
- Pass data and configuration to a component via props.
- Build a reusable, interactive UI element in React.

## Features
- Displays a preview of the text with a customizable word limit.
- Includes a toggle button to expand or collapse the text.
- Fully customizable via props (e.g., button text, color, default word count).

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd text-expander
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Run the project:
   ```bash
   npm start
   ```

## Usage
Import and use the `TextExpander` component in your React application. Below is an example of how to integrate it:

```jsx
import React from 'react';
import TextExpander from './TextExpander';

function App() {
  return (
    <div>
      <TextExpander
        collapsedNumWords={20}
        expandButtonText="Show more"
        collapseButtonText="Show less"
        buttonColor="#ff6622"
      >
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </TextExpander>
    </div>
  );
}

export default App;
```

### Props
| Prop Name           | Type   | Default     | Description                              |
|---------------------|--------|-------------|------------------------------------------|
| `collapsedNumWords` | Number | `10`        | Number of words shown when collapsed.    |
| `expandButtonText`  | String | `"Expand"`  | Text for the expand button.              |
| `collapseButtonText`| String | `"Collapse"`| Text for the collapse button.            |
| `buttonColor`       | String | `"#1a73e8"` | Color of the toggle button (hex value).  |
| `children`          | String | -           | The text content to be expanded/collapsed. |

## Component Logic
- **State**: The component uses the `useState` hook to track whether the text is expanded or collapsed.
- **Props**: Configuration options (e.g., word count, button text) are passed as props to make the component reusable.
- **Rendering**: The text is sliced based on `collapsedNumWords` when collapsed, and the full text is shown when expanded.

## Example
```jsx
<TextExpander
  collapsedNumWords={15}
  expandButtonText="Read more"
  collapseButtonText="Read less"
  buttonColor="#00cc00"
>
  This is a long paragraph that will be truncated after 15 words by default. Clicking the button will reveal the full text, demonstrating how state and props work together in React.
</TextExpander>
```

## Learning Outcomes
- Managing state with `useState` to toggle between expanded and collapsed views.
- Using props to customize the component’s behavior and appearance.
- Conditional rendering based on state changes.

## Folder Structure
```
text-expander/
├── src/
│   ├── TextExpander.js  # The main component
│   ├── App.js           # Example usage of the component
│   └── index.js         # Entry point
├── package.json         # Project dependencies and scripts
└── README.md            # This file
```

## Contributing
This is a learning exercise, but feel free to experiment! Suggestions for improvement:
- Add animations for expanding/collapsing.
- Support custom button styles beyond color.
- Allow truncation by character count instead of word count.

## License
This project is for educational purposes and does not include a formal license.

---
