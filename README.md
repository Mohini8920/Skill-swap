# SkillSwap 🎓

**Trade what you know, learn what you don't.**

SkillSwap is a modern peer-to-peer skill exchange platform where users can connect, trade expertise, and learn from each other without any money changing hands. Built with vanilla HTML/CSS/JavaScript and powered by Firebase.

---

## ✨ Features

### Core Features
- **Smart Matching Algorithm** - Finds compatible skill exchanges based on what you offer and want to learn
- **User Profiles** - Showcase your skills, availability, and bio
- **Skill Management** - Add skills you can teach and skills you want to learn
- **Browse & Filter** - Explore available skills by category (Tech, Music, Language, Culinary, Design, Fitness)
- **Match Filtering** - Filter matches by minimum score (60%, 75%, 90%+)

### Advanced Features

#### 💬 Real-Time Messaging
- Direct chat with potential skill exchange partners
- Real-time message updates using Firestore
- Message history and conversation management
- Conversation search and filtering

#### 📹 Video Call Integration
- Built-in video calling using Jitsi Meet
- One-click video call from messaging
- No third-party app needed
- Screen sharing support

#### ⭐ Reviews & Ratings
- Leave and receive reviews from exchange partners
- 5-star rating system
- Rating breakdown visualization
- View average rating on profile

#### 📅 Calendar & Booking
- Schedule skill exchange sessions
- Set date, time, and duration
- View upcoming sessions
- Session status tracking

#### 📱 Responsive Design
- Mobile-optimized interface
- Touch-friendly navigation
- Responsive grid layouts
- Works on phones, tablets, and desktops

#### 🔐 Authentication
- Email/password registration and login
- Firebase Authentication integration
- Secure session management
- Auto-login on page refresh

#### 💾 Data Persistence
- Firestore for user profiles and data
- Realtime Database for messaging
- Cloud storage ready
- Automatic syncing across devices

---

## 📖 User Guide

### Creating an Account
1. Click "Sign up free" on the home page
2. Enter first name, last name, email, and password
3. Select your primary goal (Offer skills, Learn skills, or Both)
4. Click "Create my account"

### Setting Up Your Profile
1. Click your avatar in the top right
2. Click "Edit profile"
3. Add your bio, location, and availability
4. Add skills you can teach and skills you want to learn

### Finding Matches
1. Click "Find my matches" on your profile
2. Browse recommended skill exchanges
3. Filter by minimum match score
4. Click "Request swap" to connect with someone

### Messaging
1. Click "Messages" in the top navigation
2. Select a conversation or start a new one
3. Type your message and send
4. Click "📹 Video call" to start a video call

### Scheduling Sessions
1. Click "Calendar" in the top navigation
2. Select a user from your matches
3. Choose date, time, and duration
4. Click "Schedule"
5. View upcoming sessions anytime

### Leaving Reviews
1. After a successful exchange, click "Reviews"
2. Find the user you want to review
3. Leave a rating and written review
4. Reviews help build community trust

---

## 🛠️ Technologies Used

- **Frontend**
  - HTML5
  - CSS3 (Grid, Flexbox, Variables)
  - Vanilla JavaScript (ES6+)
  - No frameworks or build tools required

- **Backend & Database**
  - Firebase Authentication
  - Firestore Database
  - Realtime Database
  - Cloud Storage (ready to use)

- **Third-Party Integration**
  - Jitsi Meet (Video Conferencing)
  - Google Fonts
  - Firebase SDKs

---

## 📊 Database Structure

### Firestore Collections

#### `users`
```javascript
{
  first: string,
  last: string,
  email: string,
  bio: string,
  location: string,
  offersSkills: [],
  wantsSkills: [],
  availability: [],
  goal: string,
  swaps: number,
  createdAt: timestamp
}
```

#### `messages/{conversationId}/chats`
```javascript
{
  from: string,
  text: string,
  timestamp: timestamp
}
```

#### `sessions`
```javascript
{
  participants: [],
  skill: string,
  scheduledDate: timestamp,
  duration: number,
  status: string,
  createdAt: timestamp
}
```

#### `reviews`
```javascript
{
  forUser: string,
  fromUser: string,
  rating: number,
  text: string,
  createdAt: timestamp
}
```

---

## 🔒 Security & Privacy

- All user data is encrypted in transit (HTTPS)
- Firestore security rules should be configured
- No payment information stored
- Messages are associated with user accounts
- Users can only see their own data by default

---

## 🚀 Deployment

### Deploy to Firebase Hosting

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize Firebase in your project
firebase init hosting

# Deploy
firebase deploy
```

### Deploy to Other Platforms
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

---

## 🐛 Known Limitations

- Google OAuth not fully implemented (ready for integration)
- Email notifications not implemented
- Admin dashboard not included
- Payment system not included
- No spam/abuse moderation system

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is open source and available under the MIT License.

---

## 💡 Future Roadmap

- [ ] Google & GitHub OAuth
- [ ] Email notifications
- [ ] Push notifications
- [ ] In-app voice calling
- [ ] File sharing
- [ ] Payment system (for optional donations)
- [ ] Admin dashboard
- [ ] Mobile apps (React Native)
- [ ] Skill verification system
- [ ] Community moderation tools

---

## 📧 Support & Feedback

For questions, issues, or feedback:
- Open an issue on GitHub
- Contact: mohini8920@github.com

---

## 🙏 Acknowledgments

- Firebase for backend infrastructure
- Jitsi Meet for video conferencing
- Google Fonts for typography
- The open-source community

---

**Built with ❤️ by Mohini Soni**

*Last updated: May 15, 2026*
