# Hedera Wallet

A comprehensive Web3 wallet application built for the Hedera network, featuring a React-based browser extension frontend and a Node.js/Express backend API.

![Hedera](https://img.shields.io/badge/Hedera-Network-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-4.9-blue)
![React](https://img.shields.io/badge/React-18.2-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📋 Overview

Hedera Wallet is a feature-rich cryptocurrency wallet designed specifically for the Hedera network. It provides users with a secure and intuitive interface to manage their digital assets, interact with domains, NFTs, and explore the Web3 ecosystem.

### Key Features

- 🔐 **Secure Wallet Management** - Create and manage multiple wallets with mnemonic phrase backup
- 💰 **Token Support** - Send, receive, and manage HBAR and other Hedera tokens
- 🎨 **NFT Gallery** - View and manage your NFT collection
- 🌐 **Domain Management** - Register and manage Web3 domains
- 📊 **Transaction History** - Track all your wallet activities
- 🌍 **Multi-language Support** - Available in 10+ languages
- 🎨 **Customizable UI** - Personalize your wallet experience with color themes
- 🔌 **Browser Extension** - Chrome extension for seamless Web3 integration

## 🏗️ Project Structure

```
Hedera-Wallet/
├── Hedera-Wallet-App/     # React Frontend (Browser Extension)
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Application pages
│   │   ├── utility/       # Helper functions and contexts
│   │   ├── i18n/          # Internationalization
│   │   └── config/        # Configuration files
│   └── public/            # Static assets and manifest
│
└── Hedera-Wallet-Node/    # Node.js Backend API
    ├── src/
    │   ├── controllers/   # API endpoint handlers
    │   ├── models/        # Database models
    │   ├── routes/        # API routes
    │   ├── middleware/    # Request middleware
    │   └── utils/         # Utility functions
    └── tests/             # Test suites
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- MongoDB (for backend)
- Chrome/Chromium browser (for extension)

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/superdev947/Hedera-Wallet.git
cd Hedera-Wallet
```

#### 2. Setup Frontend (Browser Extension)

```bash
cd Hedera-Wallet-App

# Install dependencies
npm install

# Create environment file
cp template.env .env

# Update .env with your API endpoint
# REACT_APP_API_ENDPOINT=http://your-api-endpoint

# Start development server
npm start

# Build for production
npm run build
```

#### 3. Setup Backend (API Server)

```bash
cd Hedera-Wallet-Node

# Install dependencies
npm install

# Create environment file and configure
# Add your MongoDB URI, JWT secret, Hedera credentials, etc.

# Run database migrations
npm run migration:up

# Start development server
npm run dev

# Build for production
npm run build
npm start
```

### Loading the Extension

1. Build the frontend application: `npm run build` in `Hedera-Wallet-App`
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode"
4. Click "Load unpacked"
5. Select the `Hedera-Wallet-App/build` directory

## 🔧 Configuration

### Frontend Environment Variables

Create a `.env` file in `Hedera-Wallet-App/`:

```env
REACT_APP_API_ENDPOINT=http://localhost:3000/api/
```

### Backend Environment Variables

Configure your backend environment with:

- MongoDB connection URI
- JWT secret for authentication
- Hedera network credentials
- CORS origins
- Port configuration

## 🛠️ Tech Stack

### Frontend
- **React 18.2** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **React i18next** - Internationalization
- **Formik & Yup** - Form handling and validation
- **Axios** - HTTP client
- **@hashgraph/sdk** - Hedera integration

### Backend
- **Node.js & Express** - Server framework
- **TypeScript** - Type safety
- **MongoDB & Mongoose** - Database
- **JWT** - Authentication
- **@hashgraph/sdk** - Hedera integration
- **Jest** - Testing framework

## 📱 Features

### Wallet Management
- Create new wallets with secure mnemonic generation
- Import existing wallets
- Multi-wallet support
- Wallet backup and recovery

### Transaction Features
- Send and receive HBAR
- Token transfers
- Transaction history tracking
- Real-time balance updates

### NFT Support
- View NFT collections
- NFT details and metadata
- Transfer NFTs

### Domain Services
- Domain registration
- Domain management
- Domain ticker display

### Security
- Encrypted storage
- Secure authentication
- JWT-based sessions
- Request validation middleware

## 🧪 Testing

### Frontend Tests
```bash
cd Hedera-Wallet-App
npm test
```

### Backend Tests
```bash
cd Hedera-Wallet-Node
npm test
npm run test:watch  # Watch mode
```

## 📦 Building for Production

### Frontend
```bash
cd Hedera-Wallet-App
npm run build
```

The build artifacts will be in the `build/` directory, ready to be loaded as a Chrome extension.

### Backend
```bash
cd Hedera-Wallet-Node
npm run build
```

The compiled JavaScript will be in the `dist/` directory.

## 🐳 Docker Support

The backend includes Docker support:

```bash
cd Hedera-Wallet-Node
docker build -t hedera-wallet-node .
docker run -p 3000:3000 hedera-wallet-node
```

## 🌍 Supported Languages

- English
- Spanish (Español)
- French (Français)
- German (Deutsch)
- Italian (Italiano)
- Polish (Polski)
- Arabic (العربية)
- Hindi (हिन्दी)
- Mandarin Chinese (中文)
- Japanese (日本語)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
