# Portfolio Website

A modern, responsive portfolio website built with React, Tailwind CSS, and Firebase.

## Features

- Modern UI with responsive design
- Interactive sections: Hero, About, Services, Projects, Skills, Contact
- Dark theme with gradient accents
- Project details pages with comprehensive showcases
- Firebase backend integration
- Contact form functionality
- Admin dashboard for content management
- Authentication for admin access

## Technologies Used

- **Frontend**:
  - React (Create React App)
  - React Router for navigation
  - Tailwind CSS for styling
  - Framer Motion for animations

- **Backend**:
  - Firebase Authentication
  - Firebase Firestore (database)
  - Firebase Storage (for images)
  - Firebase Hosting (deployment)

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Firebase account

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/portfolio.git
   cd portfolio
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create a Firebase project:
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project
   - Register your app with Firebase
   - Enable Authentication, Firestore, and Storage

4. Configure Firebase:
   - Create a `.env` file in the root directory
   - Add your Firebase configuration:

   ```
   REACT_APP_FIREBASE_API_KEY=your_api_key
   REACT_APP_FIREBASE_AUTH_DOMAIN=your_auth_domain
   REACT_APP_FIREBASE_PROJECT_ID=your_project_id
   REACT_APP_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
   REACT_APP_FIREBASE_APP_ID=your_app_id
   REACT_APP_FIREBASE_MEASUREMENT_ID=your_measurement_id
   ```

5. Start the development server:
   ```bash
   npm start
   # or
   yarn start
   ```

## Firebase Setup

### Security Rules

Set up Firestore and Storage security rules in your Firebase console. Sample rules are provided in the `firebase-rules.js` file.

### Authentication

1. Enable Email/Password authentication in Firebase console
2. Create an admin user:
   - Use the Firebase Authentication section to add an email/password user
   - Note: You'll need to set admin privileges manually in Firestore

### Database Structure

Create the following collections in Firestore:

1. **projects** - Store portfolio projects
   - Fields: title, description, category, type, image, mockupImage, etc.

2. **contacts** - Store form submissions
   - Fields: name, email, subject, message, createdAt, read

3. **users** - Store user roles for admin access
   - Fields: uid (match with Auth UID), role, email

### Initial Data Population

To populate initial project data:

1. Modify the data in `src/data/projectsData.js` as needed
2. Run the initialization script:
   ```bash
   node scripts/initFirebase.js
   ```

## Deployment

Deploy to Firebase Hosting:

1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```

2. Login to Firebase:
   ```bash
   firebase login
   ```

3. Initialize Firebase for your project:
   ```bash
   firebase init
   ```
   - Select Hosting
   - Choose your Firebase project
   - Set public directory to "build"
   - Configure as a single-page app (Y)
   - Don't overwrite index.html (N)

4. Build the project:
   ```bash
   npm run build
   # or
   yarn build
   ```

5. Deploy to Firebase:
   ```bash
   firebase deploy
   ```

## Folder Structure

```
portfolio/
├── public/               # Static files
├── scripts/              # Utility scripts
├── src/
│   ├── assets/           # Images and other static assets
│   ├── components/       # React components
│   ├── context/          # Context providers
│   ├── data/             # Static data
│   ├── firebase/         # Firebase services
│   ├── App.js            # Main app component
│   ├── index.js          # Entry point
│   └── index.css         # Global styles
├── .env                  # Environment variables (do not commit)
├── firebase.json         # Firebase configuration
├── firestore.rules       # Firestore security rules
├── storage.rules         # Storage security rules
└── README.md             # Project documentation
```

## Customization

1. Update personal information in components
2. Replace project images in the assets folder
3. Modify colors in `index.css` and components to match your brand
4. Update Firebase configuration in `.env` file

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [React](https://reactjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Firebase](https://firebase.google.com/)
- [React Router](https://reactrouter.com/)
- [Framer Motion](https://www.framer.com/motion/)
- [Font Awesome](https://fontawesome.com/)#   p o r t f o l i o _ c h e c k  
 