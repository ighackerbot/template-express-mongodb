# Express.js + MongoDB Backend Template

A production-ready Node.js backend template built with Express.js and MongoDB, featuring JWT authentication, file uploads, and API best practices.

## Prerequisites

- Node.js (v14+)
- npm (v6+)
- MongoDB Community Edition (v5.0+)
- Git

## Local Development Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd template-express-mongodb
```

### 2. Install Dependencies
```bash
npm install

# Install nodemon globally (recommended for development)
npm install -g nodemon
```

*Note: If you prefer not to install nodemon globally, you can run it using `npx nodemon server.js` instead of `npm run dev`.*

### 3. Set Up Environment Variables
Create a `.env` file in the root directory with the following variables:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# MongoDB Configuration
MONGODB_URI=mongodb://localhost:27017/template-express

# JWT Configuration
JWT_SECRET=your_jwt_secret_here
JWT_ISSUER=your-app-name
JWT_EXPIRES=30d

# File Uploads
UPLOADS_DIR=./uploads
PUBLIC_DIR=./public
```

### 4. Start MongoDB Service
Make sure MongoDB is running locally:

On macOS (using Homebrew):
```bash
brew services start mongodb-community
```

### 5. Start the Development Server
```bash
npm run dev
```

The server will be available at `http://localhost:3000`

## Project Structure

```
├── controllers/    # Route controllers
├── middlewares/    # Custom express middlewares
├── models/         # Mongoose models
├── routes/         # API route definitions
├── utils/          # Utility classes and functions
├── .env.example    # Example environment variables
├── server.js       # Application entry point
└── package.json
```

## Available Scripts

- `npm start` - Start production server
- `npm run dev` - Start development server with hot-reload
- `npm run lint` - Run ESLint

## API Documentation

Once the server is running, you can access the API documentation at:
- `http://localhost:3000/api-docs` (if Swagger/OpenAPI is configured)

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `PORT` | Port to run the server on | `3000` |
| `NODE_ENV` | Application environment | `development` |
| `MONGODB_URI` | MongoDB connection string | `mongodb://localhost:27017/template-express` |
| `JWT_SECRET` | Secret key for JWT signing | - |
| `JWT_ISSUER` | JWT token issuer | - |
| `JWT_EXPIRES` | JWT expiration time | `30d` |
| `UPLOADS_DIR` | Directory for file uploads | `./uploads` |
| `PUBLIC_DIR` | Directory for public assets | `./public` |

## Troubleshooting

### Nodemon Not Found
If you encounter `nodemon: command not found` when running `npm run dev`:

1. Install nodemon globally (recommended for development):
   ```bash
   npm install -g nodemon
   ```
   
2. Or install it locally as a development dependency:
   ```bash
   npm install --save-dev nodemon
   ```

3. If the issue persists, try:
   ```bash
   rm -rf node_modules package-lock.json
   npm install
   ```

## License

MIT
