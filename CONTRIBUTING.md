# Contributing to NestJS TypeScript Prisma Starter

Thank you for your interest in contributing to this starter template! This guide will help you get started with contributing to the project.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Making Changes](#making-changes)
- [Submitting Changes](#submitting-changes)
- [Style Guidelines](#style-guidelines)
- [Project Structure](#project-structure)
- [Testing](#testing)
- [Documentation](#documentation)

## 🤝 Code of Conduct

This project follows a Code of Conduct that we expect all contributors to adhere to:

- **Be respectful**: Treat everyone with respect and kindness
- **Be inclusive**: Welcome newcomers and help them learn
- **Be collaborative**: Work together towards common goals
- **Be professional**: Keep discussions focused and constructive

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **pnpm** (v8 or higher)
- **Git**
- **Docker** (optional, for database)

### Fork and Clone

1. **Fork** the repository on GitHub
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/nest-ts-prisma-starter.git
   cd nest-ts-prisma-starter
   ```
3. **Add upstream** remote:
   ```bash
   git remote add upstream https://github.com/dzikrisyairozi/nest-ts-prisma-starter.git
   ```

## 💻 Development Setup

1. **Install dependencies**:

   ```bash
   pnpm install
   ```

2. **Set up environment**:

   ```bash
   cp .env.example .env
   # Edit .env with your database configuration
   ```

3. **Set up database**:

   ```bash
   # Generate Prisma client
   pnpm run db:generate

   # Push schema to database
   pnpm run db:push

   # Seed with example data
   pnpm run db:seed
   ```

4. **Start development server**:

   ```bash
   pnpm run start:dev
   ```

5. **Verify setup**:
   - Application: http://localhost:3000
   - Swagger UI: http://localhost:3000/api

## 🛠️ Making Changes

### Branch Naming

Use descriptive branch names with the following prefixes:

- `feat/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation changes
- `style/` - Code style changes
- `refactor/` - Code refactoring
- `test/` - Test additions or changes
- `chore/` - Maintenance tasks

**Examples:**

```bash
git checkout -b feat/add-user-authentication
git checkout -b fix/resolve-database-connection-issue
git checkout -b docs/update-api-documentation
```

### Development Workflow

1. **Create a branch** for your changes:

   ```bash
   git checkout -b feat/your-feature-name
   ```

2. **Make your changes** following our [style guidelines](#style-guidelines)

3. **Test your changes**:

   ```bash
   # Run all quality checks
   pnpm run ci

   # Run specific tests
   pnpm run test
   pnpm run test:e2e
   ```

4. **Commit your changes**:

   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```

5. **Push to your fork**:
   ```bash
   git push origin feat/your-feature-name
   ```

## 📤 Submitting Changes

### Pull Request Process

1. **Update your branch** with latest upstream changes:

   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **Create a Pull Request** using our [PR template](.github/pull_request_template.md)

3. **Fill out the PR template** completely:
   - Describe what your PR does
   - Link related issues
   - Add screenshots if applicable
   - Check all boxes in the checklist

4. **Wait for review** and address any feedback

### PR Requirements

- ✅ All CI checks must pass
- ✅ Code must be properly formatted and linted
- ✅ Tests must pass (unit and e2e)
- ✅ Documentation must be updated if needed
- ✅ PR description must be clear and complete

## 🎨 Style Guidelines

### Code Style

We use automated tools to maintain consistent code style:

- **Prettier** for code formatting
- **ESLint** for code linting
- **TypeScript** for type safety

**Run formatting and linting**:

```bash
# Format code
pnpm run format

# Lint code
pnpm run lint

# Check formatting
pnpm run format:check

# Check linting
pnpm run lint:check
```

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting changes
- `refactor`: Code refactoring
- `test`: Tests
- `chore`: Maintenance

**Examples:**

```bash
feat: add user authentication with JWT
fix: resolve database connection timeout
docs: update API documentation
refactor: improve error handling in users service
```

### TypeScript Guidelines

- Use **strict TypeScript** settings
- Prefer **interfaces** over types when possible
- Use **proper typing** for all functions and variables
- Avoid `any` type - use proper types or `unknown`
- Use **async/await** instead of Promises where possible

### API Design Guidelines

- Follow **RESTful** conventions
- Use **proper HTTP status codes**
- Include comprehensive **Swagger documentation**
- Implement **proper error handling**
- Use **DTOs** for validation and documentation

## 📁 Project Structure

```
src/
├── common/          # Shared utilities and DTOs
├── prisma/          # Prisma service and module
├── users/           # Example users module
│   ├── dto/         # Data Transfer Objects
│   ├── users.controller.ts
│   ├── users.service.ts
│   └── users.module.ts
├── app.module.ts    # Root application module
└── main.ts          # Application entry point

docs/                # Documentation
├── PRISMA.md       # Prisma setup guide
└── SWAGGER.md      # Swagger documentation guide

.github/            # GitHub configurations
├── workflows/      # CI/CD pipelines
├── pull_request_template.md
└── dependabot.yml

.vscode/            # VSCode configurations
├── settings.json   # Editor settings
└── extensions.json # Recommended extensions
```

## 🧪 Testing

### Running Tests

```bash
# Unit tests
pnpm run test

# Unit tests with coverage
pnpm run test:cov

# E2E tests
pnpm run test:e2e

# Watch mode
pnpm run test:watch
```

### Writing Tests

- **Unit tests**: Test individual functions and classes
- **Integration tests**: Test module interactions
- **E2E tests**: Test complete user workflows

**Test file naming:**

- Unit tests: `*.spec.ts`
- E2E tests: `*.e2e-spec.ts`

### Test Guidelines

- Write **descriptive test names**
- Use **proper setup** and **teardown**
- **Mock external dependencies**
- Aim for **high code coverage**
- Test both **success** and **error cases**

## 📚 Documentation

### When to Update Documentation

- Adding new features
- Changing existing APIs
- Modifying configuration
- Adding new dependencies
- Changing development workflow

### Documentation Types

- **README.md**: Project overview and quick start
- **API Documentation**: Swagger/OpenAPI documentation
- **Code Comments**: Inline documentation for complex logic
- **Architecture Documentation**: High-level system design

## 🔍 Review Process

### What We Look For

- **Code Quality**: Clean, readable, maintainable code
- **Testing**: Adequate test coverage and quality
- **Documentation**: Clear and up-to-date documentation
- **Performance**: Efficient and scalable solutions
- **Security**: Secure coding practices

### Review Timeline

- **Initial Review**: Within 2-3 business days
- **Follow-up Reviews**: Within 1-2 business days
- **Merge**: After all requirements are met

## ❓ Getting Help

- **Discussions**: Use GitHub Discussions for questions
- **Issues**: Create issues for bugs or feature requests
- **Email**: Contact dzikrisyairozi@gmail.com for urgent matters

## 🎉 Recognition

Contributors will be recognized in:

- **README.md**: Contributors section
- **Release Notes**: Major contributions
- **GitHub**: Contributor graph and statistics

Thank you for contributing to making this starter template better for the community! 🚀
