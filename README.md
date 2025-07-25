# Paste App

A modern, feature-rich pastebin clone built with Next.js, allowing users to share text snippets and code with ease.

## 🚀 Live Demo

**[View Live Application](https://paste-app-chi.vercel.app)**

## ✨ Features

- **Quick Text Sharing**: Paste and share text snippets instantly
- **Syntax Highlighting**: Support for multiple programming languages
- **Expiration Options**: Set custom expiration times for pastes
- **Shareable Links**: Generate unique URLs for each paste
- **Clean Interface**: Modern, responsive design
- **No Registration Required**: Start sharing immediately
- **Mobile Friendly**: Optimized for all device sizes

## 🛠️ Tech Stack

- **Frontend**: Next.js, React
- **Styling**: Tailwind CSS
- **Database**: MongoDB
- **Deployment**: Vercel
- **Language**: TypeScript/JavaScript

## 🎯 Use Cases

- Share code snippets with colleagues
- Store temporary notes and configurations
- Share logs and error messages
- Collaborate on text-based content
- Quick text sharing without email

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB database

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/paste-app.git
   cd paste-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```
   
   Configure your environment variables:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   NEXTAUTH_SECRET=your_secret_key
   NEXT_PUBLIC_BASE_URL=http://localhost:3000
   ```

4. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📱 Usage

1. **Create a Paste**
   - Visit the homepage
   - Enter your text or code
   - Select syntax highlighting (optional)
   - Set expiration time (optional)
   - Click "Create Paste"

2. **Share Your Paste**
   - Copy the generated URL
   - Share with anyone via email, chat, or social media

3. **View Pastes**
   - Access pastes via their unique URLs
   - View with syntax highlighting
   - Copy content easily

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `MONGODB_URI` | MongoDB connection string | Yes |
| `NEXTAUTH_SECRET` | Secret for authentication | Yes |
| `NEXT_PUBLIC_BASE_URL` | Base URL of the application | Yes |

### Database Schema

The application uses MongoDB with the following collection structure:

```javascript
{
  _id: ObjectId,
  content: String,
  language: String,
  expiresAt: Date,
  createdAt: Date,
  slug: String,
  views: Number
}
```

## 🚀 Deployment

### Deploy on Vercel

1. **Connect your repository** to Vercel
2. **Set environment variables** in Vercel dashboard
3. **Deploy** - Vercel will automatically build and deploy

### Deploy on other platforms

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Start the production server**
   ```bash
   npm start
   ```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/paste` | Create a new paste |
| GET | `/api/paste/[id]` | Retrieve a specific paste |
| DELETE | `/api/paste/[id]` | Delete a paste (if owner) |

## 🛡️ Security Features

- Input sanitization to prevent XSS attacks
- Rate limiting to prevent spam
- Automatic cleanup of expired pastes
- No sensitive data logging

## 📈 Performance

- Server-side rendering with Next.js
- Optimized MongoDB queries
- CDN delivery via Vercel
- Responsive image loading
- Minimal JavaScript bundle

## 🐛 Known Issues

- Large pastes (>1MB) may have slower load times
- Some special characters may not display correctly in certain browsers

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - *Initial work* - [YourGitHub](https://github.com/yourusername)

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- Vercel for hosting and deployment
- MongoDB for the database solution
- Tailwind CSS for the styling system

## 📞 Support

If you have any questions or need help, please:

- Open an issue on GitHub
- Contact us at support@yourapp.com
- Visit our documentation at [docs.yourapp.com](https://docs.yourapp.com)

---

**Built with ❤️ using Next.js and deployed on Vercel**
