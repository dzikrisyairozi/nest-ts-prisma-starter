<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

A comprehensive [Nest](https://github.com/nestjs/nest) framework TypeScript starter repository with Prisma, enhanced with a complete development environment including:

- 🎨 **Prettier** - Code formatting
- 🔍 **ESLint** - Code linting with TypeScript support
- 🐕 **Husky** - Git hooks for automated quality checks
- 📝 **Commitlint** - Conventional commit message linting
- 🚀 **Lint-staged** - Run linters on staged files
- 🔧 **Pre-configured scripts** - Ready-to-use development workflows

## Project setup

```bash
$ pnpm install
```

## Compile and run the project

```bash
# development
$ pnpm run start

# watch mode
$ pnpm run start:dev

# production mode
$ pnpm run start:prod
```

## Run tests

```bash
# unit tests
$ pnpm run test

# e2e tests
$ pnpm run test:e2e

# test coverage
$ pnpm run test:cov
```

## Development Tools

### Code Quality & Formatting

```bash
# Format code with Prettier
$ pnpm run format

# Check formatting without fixing
$ pnpm run format:check

# Lint and fix code with ESLint
$ pnpm run lint

# Check linting without fixing
$ pnpm run lint:check

# Type checking
$ pnpm run type-check
```

### Git Hooks (Husky)

This project includes several automated git hooks:

- **commit-msg**: Validates commit messages using commitlint
- **pre-commit**: Runs lint-staged (formatting and linting on staged files)
- **pre-push**: Runs type checking, linting, and tests before pushing
- **post-merge**: Automatically installs dependencies if package files changed

### Commit Message Convention

This project follows the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools
- `perf`: A code change that improves performance
- `ci`: Changes to CI configuration files and scripts
- `build`: Changes that affect the build system or external dependencies
- `revert`: Reverts a previous commit

**Examples:**

```bash
feat: add user authentication
fix: resolve memory leak in data processing
docs: update API documentation
```

## CI/CD Pipeline

This project includes a comprehensive CI/CD pipeline using GitHub Actions:

### 🔄 **Single CI/CD Pipeline** (.github/workflows/ci.yml)

- **Triggers**: Push to main branch, Pull requests
- **All-in-One**: Quality checks, testing, security, build, and deploy in single job
- **Quality Checks**: Type checking, linting, formatting validation
- **Testing**: Unit tests, E2E tests, coverage reports
- **Security**: Dependency audit, CodeQL analysis
- **Build**: Application build and artifact upload
- **Deploy**: Staging and production deployments

### 🚀 **Release Management** (.github/workflows/release.yml)

- **Triggers**: Git tags (v\*)
- **Automated Releases**: GitHub releases with changelogs
- **Docker Images**: Container builds for deployment
- **Production Deploy**: Automatic production deployment

### 🤖 **Dependency Management** (.github/dependabot.yml)

- **Weekly Updates**: Single PR per week with all updates
- **Comprehensive**: All dependencies updated together
- **Security Updates**: Automatic security patches

### 🛡️ **Security Features**

- CodeQL security scanning
- Dependency vulnerability checks
- Branch protection rules
- Environment-based deployments with approvals

### 📊 **Monitoring & Notifications**

- Test coverage reports (Codecov integration)
- Slack notifications for deployments
- Build status badges
- Performance tracking

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ pnpm install -g mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
