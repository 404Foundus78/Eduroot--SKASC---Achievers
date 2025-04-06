# Eduroot--SKASC---Achievers
EduRoot is a Flutter-based educational app built for the Google Solution Challenge. It combines mental health awareness with personalized learning by offering age-based assessments, mental wellness tracking, and curated educational content, integrating Firebase and Google tools for a smarter student experience.

# EduRoot – Smart Learning with Mental Health Awareness

EduRoot is a Flutter-based educational platform designed for the **Google Solution Challenge**. It focuses on student well-being and learning by combining mental health assessments with personalized educational content.

---

## Features

- **User Authentication**  
  Secure and simple login/signup using Firebase Authentication.

- **Age-Based Mental Health Assessment**  
  Users above 15 years are prompted with 10 mental health questions to determine study readiness. Option to skip is available.

- **Mental Health Portfolio**  
  A personalized dashboard that shows the user's mental health evaluation results.

- **Educational Content Hub**  
  Access learning resources like videos, notes, and more based on the user's need and ability.

- **Google Tools Integration**  
  Includes at least two Google technologies to enhance learning and health analysis (e.g., Firebase, Google Sheets API).

---

## Tech Stack

- **Flutter** – Cross-platform UI framework  
- **Dart** – Programming language  
- **Firebase** – Authentication, Firestore, Analytics  
- **Google Sheets / Google Forms** – For tracking and reporting  
- **Cloud Firestore** – Database management  

---

## Getting Started

### Prerequisites

- Flutter SDK installed  
- Dart SDK  
- Firebase account  
- Android Studio or VS Code  

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/eduroot.git
cd eduroot

Installation Dependencies
flutter pub get

Connect Firebase



Create a Firebase project

Add Android/iOS app

Download and place google-services.json (Android) or GoogleService-Info.plist (iOS) in the respective directories

Enable Firebase Authentication and Firestore in Firebase Console

RUN THE APP
flutter run

Folder Structure
lib/
├── main.dart
├── screens/
│   ├── login.dart
│   ├── signup.dart
│   ├── assessment.dart
│   ├── dashboard.dart
│   └── content_page.dart
├── services/
│   ├── auth_service.dart
│   └── database_service.dart
├── widgets/
│   └── custom_widgets.dart

Future Scope

Add personalized study plans based on mental health data

Integrate AI-driven recommendations

Real-time chat support for students

Gamified learning progress tracking



---

Contribution

Feel free to fork this repo and submit pull requests. All kinds of contributions are welcome – bug fixes, features, documentation, or suggestions.

Developers

Team As Mentioned in Solution Challenge PPT

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>EduRoot Chatbot</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f0f4f8;
    }
    #chatContainer {
      background: white;
      padding: 20px;
      border-radius: 10px;
      max-width: 500px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    #chatInput {
      width: 80%;
      padding: 10px;
      margin-right: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    #sendBtn {
      padding: 10px 15px;
      background: #007BFF;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    #sendBtn:hover {
      background: #0056b3;
    }
    #chatResponse {
      margin-top: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div id="chatContainer">
    <h2>EduRoot Chatbot</h2>
    <input type="text" id="chatInput" placeholder="Ask me anything..."/>
    <button id="sendBtn" onclick="sendChat()">Send</button>
    <div id="chatResponse"></div>
  </div>

  <script>
    function sendChat() {
      const input = document.getElementById("chatInput").value.toLowerCase();
      const response = document.getElementById("chatResponse");

      const replies = [
        { keywords: ["math", "algebra", "geometry"], reply: "Math is a core skill! You can start with our mathematics videos." },
        { keywords: ["history", "world war", "ancient"], reply: "History is fascinating! Check out our world history content." },
        { keywords: ["science", "physics", "chemistry", "biology"], reply: "Science helps us understand the world. Visit the science section." },
        { keywords: ["ui", "ux", "design", "interface"], reply: "UI/UX Design is all about user experience. Try our design tutorials!" },
        { keywords: ["mental", "stress", "health", "depression"], reply: "Mental health is important. You can revisit the wellness check or talk to someone you trust." },
        { keywords: ["language", "notes", "tamil", "malayalam"], reply: "You can select your preferred language in the notes section!" },
        { keywords: ["hello", "hi", "hey"], reply: "Hello! How can I assist you today?" },
        { keywords: ["bye", "thank", "goodbye"], reply: "You're welcome! Feel free to return anytime!" },
        { keywords: ["video", "content", "learn"], reply: "We offer videos in many subjects. Check out the educational videos section." }
      ];

      let foundReply = "Hmm... I’m still learning. Can you ask in a different way or be more specific?";

      for (const item of replies) {
        for (const keyword of item.keywords) {
          if (input.includes(keyword)) {
            foundReply = item.reply;
            break;
          }
        }
        if (foundReply !== "Hmm... I’m still learning. Can you ask in a different way or be more specific?") break;
      }

      response.innerText = foundReply;
    }
  </script>

</body>
</html>

function sendChat() {
  const input = document.getElementById("chatInput").value.toLowerCase();
  const response = document.getElementById("chatResponse");

  const replies = [
    { keywords: ["math", "algebra", "geometry"], reply: "Math is a core skill! You can start with our mathematics videos." },
    { keywords: ["history", "world war", "ancient"], reply: "History is fascinating! Check out our world history content." },
    { keywords: ["science", "physics", "chemistry", "biology"], reply: "Science helps us understand the world. Visit the science section." },
    { keywords: ["ui", "ux", "design", "interface"], reply: "UI/UX Design is all about user experience. Try our design tutorials!" },
    { keywords: ["mental", "stress", "health", "depression"], reply: "Mental health is important. You can revisit the wellness check or talk to someone you trust." },
    { keywords: ["language", "notes", "tamil", "malayalam"], reply: "You can select your preferred language in the notes section!" },
    { keywords: ["hello", "hi", "hey"], reply: "Hello! How can I assist you today?" },
    { keywords: ["bye", "thank", "goodbye"], reply: "You're welcome! Feel free to return anytime!" },
    { keywords: ["video", "content", "learn"], reply: "We offer videos in many subjects. Check out the educational videos section." }
  ];

  let foundReply = "Hmm... I’m still learning. Can you ask in a different way or be more specific?";

  for (const item of replies) {
    for (const keyword of item.keywords) {
      if (input.includes(keyword)) {
        foundReply = item.reply;
        break;
      }
    }
    if (foundReply !== "Hmm... I’m still learning. Can you ask in a different way or be more specific?") break;
  }

  response.innerText = foundReply;
}
