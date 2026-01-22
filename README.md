# Chatbot Design
This project is a responsive chat interface built with React to simulate a conversational agent using pre-determined responses. The project utilises React hooks, component modularity, and asynchronous state management.

## Structure of Repository
```
├── public
├── src
│   ├── assets
│   ├── components
│   │   ├── ChatInput.css
│   │   ├── ChatInput.jsx
│   │   ├── ChatMessage.css
│   │   ├── ChatMessage.jsx
│   │   ├── ChatMessages.css
│   │   └── ChatMessages.jsx
│   ├── App.cs
│   ├── App.jsx
│   ├── index.css
│   └── main.js
└── README.md
```

## Technical Implementation
* **React Hooks:** Extensively utilized core hooks to manage application logic:
  * `useState:` Managed the array of chat messages and input field state.
  * `useEffect:` Handled side effects like synchronizing messages with localStorage and initializing the chatbot's response rules on mount.
  * `useRef:` Implemented direct DOM manipulation to auto-scroll the chat window to the most recent message.
* **Custom Hooks:** Engineered a useAutoScroll hook to abstract the scrolling logic, promoting code reusability and cleaner component architecture.
* **Asynchronous Handling:** Implemented async/await patterns to simulate network latency and handle the asynchronous nature of the simulated bot responses, including a loading state UI.
* **Component Modularity:** Decomposed the UI into reusable components (ChatInput, ChatMessage, ChatMessages) to isolate concerns and improve maintainability.
* **Data Persistence:** Integrated localStorage to retain conversation history across browser sessions, parsing JSON data on initialization.
* **Time Formatting:** Integrated the dayjs library to generate and format precise timestamps for every message sent and received.

# Key Features
* **Simulated AI Response:** The bot replies to specific keywords (e.g., "hello", "goodbye", "roll a dice", "coin toss", etc) with pre-determined responses and can also generate dynamic content like unique IDs.
* **Loading States:** Displays a visual loading spinner GIF while waiting for the "bot" to generate a response.
* **Auto-Scrolling:** The chat window automatically scrolls to the bottom whenever a new message arrives, ensuring the latest content is always visible.
* **Keyboard Accessibility:** Users can send messages using the Enter key and clear the input field using Escape.
* **Message Timestamps:** Every message displays the exact time it was sent, formatted for readability (e.g., "2:30pm").

## How to Run
**1) Installing the relevant dependencies -** Navigate to the project folder and run the following code.
```
npm install
```
<br>

**2) Starting the dev server -** Run the Vite development server with the following code.
```
npm run dev
```

<br>
<img width="1919" height="869" alt="Screenshot 2026-01-23 014515" src="https://github.com/user-attachments/assets/989bb884-4d38-4f87-942f-86dbd332b59c" />

