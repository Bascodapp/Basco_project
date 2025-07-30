# Basco_project

Next.js Project with Supabase, shadcn/ui, and Tailwind CSS
Test Integration Tests

This is a modern web application built with Next.js, featuring Supabase for backend services, shadcn/ui for beautiful UI components, and Tailwind CSS for styling.

Development Options
You can develop this project in two ways:

1. Using Dev Container (Recommended)
The easiest way to get started is using VS Code's Dev Containers. This approach provides a consistent development environment with all necessary tools pre-installed.

Prerequisites:

VS Code
Docker Desktop
Dev Containers extension
Steps:

Clone the repository
Open in VS Code
When prompted, click "Reopen in Container"
Wait for the container to build and initialize
The setup script will run automatically and configure everything
2. Local Development
If you prefer to develop locally, ensure you have these prerequisites:

Node.js (Latest LTS version recommended)
npm or yarn
Docker (for running Supabase locally)
jq (for JSON processing in setup script)
Getting Started
Clone the repository

git clone <repository-url>
cd <project-directory>
Install dependencies

npm install
# or
yarn install
Run the setup script

npm run setup
# or
yarn setup
This script will:

Install Supabase CLI if not present
Start a local Supabase instance
Configure your environment variables
Generate TypeScript types for Supabase
After running the script, you'll have access to:

Local Supabase instance
Supabase Studio at http://localhost:54423
Automatically configured .env.local file
Start the development server

npm run dev
# or
yarn dev
Generate Supabase Types (when schema changes)

npm run types:generate
Project Structure
/app - Next.js app router pages and layouts
/components - Reusable UI components
/lib - Utility functions and shared logic
/utils - Helper functions and utilities
/supabase - Supabase related configurations
/src - Source code including types and other core functionality
Available Scripts
npm run dev - Start development server
npm run build - Build the application for production
npm run start - Start the production server
npm run types:generate - Generate Supabase TypeScript types
Testing Scripts
npm run test - Run unit tests
npm run test:watch - Run unit tests in watch mode
npm run test:cucumber - Run Cucumber integration tests (standard)
npm run test:cucumber:fast - Run Cucumber tests with 2 workers (faster)
npm run test:cucumber:silent - Run Cucumber tests with 4 workers (fastest)
npm run test:cucumber:ci - Run Cucumber tests for CI with Allure reporting
npm run test:report:generate - Generate Allure HTML report
npm run test:report:open - Open Allure report in browser
npm run test:report:serve - Serve Allure report temporarily
npm run test:ci - Run all CI tests and generate reports
Features
Modern React with Next.js App Router
Server-side rendering and static generation
Type-safe database operations with Supabase
Beautiful and accessible UI components from shadcn/ui
Responsive design with Tailwind CSS
Dark mode support with next-themes
Form validation with React Hook Form and Zod
Efficient data fetching with TanStack Query
Testing
This project includes comprehensive testing with multiple layers:

Unit Tests
Framework: Vitest with React Testing Library
Location: Test files alongside source code (*.test.ts, *.test.tsx)
Run: npm run test or npm run test:watch
Integration Tests
Framework: Cucumber with Gherkin syntax
Location: test/features/ directory
Features: BDD scenarios testing complete user workflows
Database: Full Supabase instance with real data
Performance: Optimized with parallel execution (2.6s vs 6s)
Test Reports
Allure Reports: Beautiful HTML reports with step-by-step details
CI Integration: Automatic report generation and GitHub Pages publishing
PR Comments: Test summaries automatically posted to pull requests
Artifacts: Reports stored as GitHub Actions artifacts for 30 days
Running Tests Locally
# Quick unit tests
npm run test

# Fast integration tests (recommended for development)
npm run test:cucumber:fast

# Full integration test suite with reporting
npm run test:cucumber:ci
npm run test:report:serve  # Opens report in browser
CI/CD Testing
Triggers: All pushes and pull requests
Parallel Jobs: Lint, unit tests, database tests, integration tests
Environment: Automated Supabase instance with migrations
Reports: Allure reports published to GitHub Pages on main branch
Styling
This project uses Tailwind CSS for styling. The configuration can be found in:

tailwind.config.ts - Tailwind configuration
postcss.config.js - PostCSS configuration
Contributing
Fork the repository
Create your feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add some amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Next.js Documentation
Supabase Documentation
shadcn/ui Documentation
Tailwind CSS Documentation
