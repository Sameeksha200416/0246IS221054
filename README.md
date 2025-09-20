# URL Shortener

A modern, feature-rich URL shortener application built with React. This application allows users to create shortened URLs with custom aliases, track analytics, and manage expiration times.

## ✨ Features

- **URL Shortening**: Convert long URLs into short, manageable links
- **Custom Short Codes**: Create personalized short codes for your URLs
- **Expiration Control**: Set custom expiration times for shortened URLs (default: 30 minutes)
- **Bulk Processing**: Create multiple shortened URLs at once (up to 5 URLs simultaneously)
- **QR Code Generation**: Automatically generate QR codes for shortened URLs
- **Analytics & Statistics**: Track click counts, referrers, user agents, and geographical data
- **User Authentication**: Secure login system with multiple providers
- **Responsive Design**: Mobile-friendly interface built with Material-UI
- **Protected Routes**: Secure access to analytics and statistics

## 🛠️ Technology Stack

- **Frontend Framework**: React 19.1.1
- **UI Library**: Material-UI (MUI) 7.3.2
- **Styling**: Tailwind CSS 3.4.17
- **Routing**: React Router DOM 7.9.1
- **QR Code Generation**: qrcode 1.5.4
- **Build Tool**: Create React App with CRACO
- **State Management**: React Context API

## 📁 Project Structure

```
src/
├── components/
│   ├── Navigation.jsx      # Navigation bar component
│   └── ProtectedRoute.jsx  # Route protection wrapper
├── contexts/
│   └── AuthContext.js      # Authentication context
├── hooks/
│   └── useFormValidation.js # Form validation hook
├── pages/
│   ├── LoginPage.jsx       # User authentication page
│   ├── Redirector.jsx      # URL redirection handler
│   ├── ShortnerPage.jsx    # Main URL shortening interface
│   └── StatsPage.jsx       # Analytics and statistics
├── services/
│   └── authService.js      # Authentication service
└── utils/
    ├── authHelpers.js      # Authentication utilities
    ├── helpers.js          # General utility functions
    ├── loggingAdapter.js   # Logging functionality
    ├── storage.js          # Local storage management
    └── tokenManager.js     # JWT token management
```

## 🚀 Getting Started

### Prerequisites

- Node.js (version 14 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd url-shortener
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📖 Usage

### Creating Shortened URLs

1. **Navigate to the main page** (`/`)
2. **Enter your long URL** in the input field
3. **Set expiration time** (optional, defaults to 30 minutes)
4. **Add custom short code** (optional, system generates one if not provided)
5. **Click "Shorten"** to create your shortened URL
6. **Copy the generated short URL** or scan the QR code

### Viewing Analytics

1. **Navigate to the Statistics page** (`/stats`)
2. **View comprehensive analytics** including:
   - Total click counts
   - Click timestamps
   - Referrer information
   - User agent details
   - Geographical data

### Authentication

1. **Visit the Login page** (`/login`)
2. **Sign in using your preferred method**
3. **Access protected features** like detailed analytics

## 🔗 API Routes

- `/` - Main URL shortening interface
- `/login` - User authentication
- `/stats` - Analytics and statistics (protected)
- `/go/:shortcode` - URL redirection endpoint

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
REACT_APP_API_BASE_URL=your_api_base_url
REACT_APP_DEFAULT_EXPIRY_MINUTES=30
```

### Tailwind CSS

The project uses Tailwind CSS for styling. Configuration can be found in `tailwind.config.js`.

### CRACO Configuration

Custom webpack configuration is managed through CRACO. See `craco.config.js` for details.

## 🔧 Available Scripts

### `npm start`
Runs the app in development mode at [http://localhost:3000](http://localhost:3000)

### `npm test`
Launches the test runner in interactive watch mode

### `npm run build`
Builds the app for production to the `build` folder

### `npm run eject`
**Note**: This is a one-way operation. Ejects from Create React App configuration.

## 📊 Features in Detail

### URL Validation
- Validates URLs using native URL constructor
- Supports both HTTP and HTTPS protocols
- Provides real-time feedback for invalid URLs

### Short Code Generation
- Generates random alphanumeric codes (default: 6 characters)
- Allows custom short codes with validation
- Ensures uniqueness of generated codes

### Data Storage
- Uses browser's localStorage for data persistence
- Stores URL mappings, click analytics, and user sessions
- Implements expiration checking for automatic cleanup

### Security Features
- JWT token-based authentication
- Protected routes with authentication guards
- Secure token management and validation

## 🎨 UI/UX Features

- **Material Design**: Modern, clean interface using Material-UI
- **Responsive Layout**: Optimized for mobile and desktop devices
- **Loading States**: Visual feedback during operations
- **Error Handling**: User-friendly error messages
- **Animations**: Smooth transitions and micro-interactions

## 🧪 Testing

The project includes testing setup with:
- React Testing Library
- Jest DOM matchers
- User event simulation

Run tests with:
```bash
npm test
```

## 🔒 Security Considerations

- **URL Validation**: Prevents malicious URL injection
- **Authentication**: Secure user authentication system
- **Token Management**: Proper JWT token handling
- **Input Sanitization**: Validates all user inputs

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

The build folder will contain optimized production files ready for deployment.

### Deployment Options

- **Static Hosting**: Netlify, Vercel, GitHub Pages
- **CDN**: AWS CloudFront, Cloudflare
- **Traditional Hosting**: Any web server with static file support

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [Create React App](https://create-react-app.dev/)
- UI components from [Material-UI](https://mui.com/)
- Styling with [Tailwind CSS](https://tailwindcss.com/)
- QR code generation by [qrcode](https://www.npmjs.com/package/qrcode)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
