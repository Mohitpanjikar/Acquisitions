# Acquisitions

A modern Node.js REST API built with Express.js, Drizzle ORM, and Neon (Serverless PostgreSQL).

## Tech Stack

- **Runtime:** Node.js (ES Modules)
- **Framework:** Express.js 5
- **Database:** Neon (Serverless PostgreSQL)
- **ORM:** Drizzle ORM
- **Linting:** ESLint with Prettier

## Project Structure

```
├── src/
│   ├── config/        # Configuration files (database, environment)
│   ├── controllers/   # Route controllers (request handlers)
│   ├── middleware/    # Express middleware
│   ├── models/        # Drizzle schema definitions
│   ├── routes/        # API route definitions
│   ├── services/      # Business logic layer
│   ├── utils/         # Utility functions and helpers
│   ├── validations/   # Request validation schemas
│   ├── app.js         # Express app configuration
│   ├── index.js       # Application entry point
│   └── server.js      # Server startup
├── eslint.config.js   # ESLint configuration
├── package.json
└── .env.example       # Environment variables template
```

## Prerequisites

- Node.js 18+
- npm or yarn
- Neon database account (https://neon.tech)

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Mohitpanjikar/Acquisitions.git
cd Acquisitions
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Add your environment variables:

```env
# Server
PORT=3000
NODE_ENV=development

# Database (Neon)
DATABASE_URL=postgresql://user:password@host/database?sslmode=require
```

### 4. Run the development server

```bash
npm run dev
```

The server will start at `http://localhost:3000`

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with watch mode |
| `npm run lint` | Run ESLint to check for code issues |
| `npm run lint:fix` | Run ESLint and auto-fix issues |
| `npm run format` | Format code with Prettier |
| `npm run format:check` | Check code formatting |

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Health check / Welcome message |

> More endpoints will be documented as they are added.

## Database

This project uses [Drizzle ORM](https://orm.drizzle.team/) with [Neon](https://neon.tech/) serverless PostgreSQL.

### Running Migrations

```bash
npx drizzle-kit generate   # Generate migrations
npx drizzle-kit migrate    # Apply migrations
npx drizzle-kit studio     # Open Drizzle Studio (database GUI)
```

## Development

### Code Style

This project uses ESLint and Prettier for code quality and formatting:

- **ESLint:** Enforces coding standards and catches errors
- **Prettier:** Ensures consistent code formatting

```bash
# Check for linting issues
npm run lint

# Auto-fix linting issues
npm run lint:fix

# Format all files
npm run format
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Author

Mohit Panjikar

---

Made with ❤️
