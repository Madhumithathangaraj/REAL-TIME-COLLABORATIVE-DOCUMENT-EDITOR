# REAL-TIME-COLLABORATIVE-DOCUMENT-EDITOR
COMPANY": CODTECH IT SOLUTION 
"NAME':MADHUMITHA T 
INTERN ID":CTO4WG146 
"DOMAIN":FULL STACK WEB DEVELOPMENT
"DURATION":4 WEEKS 
"MENTOR":NEELS SANTHOSH 
A Real-Time Collaborative Document Editor is a web-based application where multiple users can edit the same document at the same time, and everyone sees changes live, instantly, without needing to refresh the page.

Think:
🔹 Google Docs
🔹 Microsoft Word Online

 Key Features
Feature	Description
✍️ Live editing	Everyone sees changes instantly.
👥 Multi-user support	Many users can edit the document together.
🔄 Real-time sync	Changes are synced across devices using WebSockets or similar.
💾 Auto-saving	The document is continuously saved to the database.
🔐 Authentication (optional)	Only logged-in users can edit/view.
1. Frontend (React/Vue)
Rich text editor (like a <textarea>, Slate.js, or Tiptap)

Captures user input

Sends changes to backend via WebSocket

Displays updates from other users live

2. Backend (Node.js / Python)
Uses WebSocket (e.g. with Socket.io) to keep a persistent connection with all users

When one user types something:

It sends the change to the server

The server broadcasts it to other connected users

Saves the updated content to a database like MongoDB/PostgreSQL

3. Database (MongoDB / PostgreSQL)
Stores the document’s current content

Used to:

Load document when a user joins

Persist edits for future use

🔁 Real-Time Example
Imagine two users are editing the same doc:

User A types "Hello"

The frontend captures this.

It sends "Hello" to the backend via WebSocket.
![Image](https://github.com/user-attachments/assets/ec952729-9de1-4231-b789-6b32a2b80097)

Backend updates the doc in the DB.

Backend broadcasts "Hello" to User B.

User B sees "Hello" instantly appear in the editor.

