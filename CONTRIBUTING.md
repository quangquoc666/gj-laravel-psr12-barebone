# Contributing Guidelines

## Introduction

We are thrilled that you are interested in contributing to the Laravel PSR12 Barebone project! Every contribution is valuable.

## Contribution Process

1. **Fork the Project**
   - Fork this repository to your GitHub account
   - Clone the forked repository to your local machine

2. **Create a Branch**
   ```bash
   git checkout -b feature/feature-name
   ```

3. **Make Changes**
   - Follow coding standards
   - Write clear, readable code
   - Add/update tests if necessary

## CI/CD Contribution Guidelines

### GitHub Actions Workflow

We welcome contributions to improve our CI/CD pipeline. Key areas for contribution:

- Enhance existing workflows
- Add new deployment strategies
- Improve test coverage
- Optimize build times
- Support additional platforms/environments

#### Workflow Location
`/.github/workflows/laravel.yml`

#### Contribution Suggestions:
- Add more comprehensive testing
- Implement caching strategies
- Create matrix builds for multiple PHP/Laravel versions
- Add performance profiling
- Integrate code quality tools

### Workflow Validation

Before submitting a PR for CI/CD improvements:
```bash
# Validate GitHub Actions workflow
act -j laravel-tests  # Requires 'act' CLI
# or use GitHub's web interface workflow validator
```

## Code Verification

```bash
# Run PHPStan
vendor/bin/phpstan analyse

# Check code style
vendor/bin/pint

# Run tests
php artisan test
```

## Commit Changes
- Use [Conventional Commits](https://www.conventionalcommits.org/)
```bash
git commit -m "feat(ci): improve GitHub Actions workflow"
```

## Create Pull Request
- Describe changes in detail
- Link to related issues
- Explain the motivation behind CI/CD improvements

## System Requirements

- PHP 8.4+
- Composer
- Docker
- Node.js 18+
- GitHub Actions CLI (act) - recommended

## Code of Conduct

- Respect
- Professionalism
- Collaboration

## Questions?

Contact: contact@example.com

**Thank you for helping improve our CI/CD infrastructure!**
