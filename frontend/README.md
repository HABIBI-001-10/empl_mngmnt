# Employee Management System — Frontend

A modern frontend application for the **Employee Management System**, built using **React, TypeScript, and Vite**.

## Tech Stack

* **React** — Frontend UI library
* **TypeScript** — Type-safe development
* **Vite** — Development server and build tool
* **ESLint** — Code quality and linting
* **npm** — Package management

## Project Structure

```text
frontend/
│
├── public/                 # Public/static assets
├── src/                    # Application source code
│   ├── assets/             # Images and other assets
│   ├── components/         # Reusable UI components
│   ├── pages/              # Application pages
│   ├── services/           # API and backend communication
│   ├── App.tsx             # Main application component
│   └── main.tsx            # Application entry point
│
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── package-lock.json
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
├── vite.config.ts
└── README.md
```

> The `src` structure may change as the application grows.

## Getting Started

### Prerequisites

Make sure the following are installed:

* [Node.js](https://nodejs.org/)
* npm
* Git

Check your installation:

```bash
node --version
npm --version
git --version
```

## Installation

Clone the repository:

```bash
git clone <repository-url>
```

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

## Development

Start the development server:

```bash
npm run dev
```

Vite will provide a local development URL, usually:

```text
http://localhost:5173
```

Open the URL in your browser to access the application.

## Production Build

Create a production build:

```bash
npm run build
```

The optimized production files will be generated in:

```text
dist/
```

## Preview Production Build

To preview the production build locally:

```bash
npm run preview
```

## Linting

Run ESLint:

```bash
npm run lint
```

Make sure linting passes before pushing changes to the repository.

## Backend Integration

The frontend is designed to communicate with the Employee Management System backend through REST APIs.

```text
┌──────────────────────────┐
│      React Frontend      │
│   React + TypeScript     │
└────────────┬─────────────┘
             │
             │ REST API
             ▼
┌──────────────────────────┐
│       Backend API        │
│   Authentication / CRUD  │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│         Database         │
└──────────────────────────┘
```

## Environment Variables

If the backend API URL is configured through environment variables, create a `.env` file:

```env
VITE_API_URL=http://localhost:8000/api
```

Access it in TypeScript using:

```typescript
const API_URL = import.meta.env.VITE_API_URL;
```

Do not commit sensitive credentials, tokens, or secrets to GitHub.

## Git Workflow

For team development, use feature branches instead of directly modifying `main`.

Example:

```text
main
 │
 └── develop
      │
      ├── feature/dashboard
      ├── feature/employee-management
      ├── feature/authentication
      └── feature/profile
```

Create a feature branch:

```bash
git checkout -b feature/employee-management
```

Check your changes:

```bash
git status
```

Stage changes:

```bash
git add .
```

Commit:

```bash
git commit -m "Add employee management UI"
```

Push:

```bash
git push origin feature/employee-management
```

## Available Commands

| Command           | Description                  |
| ----------------- | ---------------------------- |
| `npm install`     | Install project dependencies |
| `npm run dev`     | Start development server     |
| `npm run build`   | Create production build      |
| `npm run lint`    | Run ESLint                   |
| `npm run preview` | Preview production build     |

## Development Guidelines

* Use **TypeScript** for all new components.
* Create reusable components whenever possible.
* Keep API communication inside dedicated service files.
* Do not hard-code API URLs.
* Do not commit `.env` files containing secrets.
* Run `npm run lint` before committing.
* Run `npm run build` before creating a pull request.
* Use meaningful Git commit messages.
* Develop new features using separate branches.

## Future Modules

The frontend can be expanded with modules such as:

* Dashboard
* Employee Management
* Department Management
* Attendance
* Leave Management
* Payroll
* Employee Profiles
* Authentication & Authorization
* Notifications
* Reports & Analytics
* Admin Management

## License

This project is intended for **company/internal use**.
