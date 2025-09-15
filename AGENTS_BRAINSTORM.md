# 🚨 Critical Notes
- **Filament v4**: The project will use Filament v4. There are significant changes compared to v3. When encountering errors due to v3 syntax, note them immediately below.
- **Project Name**: gj-backstage - backstage management system
- **Tech Stack**: Laravel 12 + TailwindCSS v4 + Pest v4 (latest versions)
- **Status**: Fresh installation - no business logic yet

# 📋 Project Context
## Overview
- **Purpose**: Backstage management system (need to clarify business requirements more precisely)
- **Database**: PostgreSQL
- **Timezone**: GMT+7 (Ho Chi Minh)

## Current Architecture
### Backend
- **Laravel 12.28.1**: New streamlined structure (bootstrap/app.php)
- **No Kernel files**: Commands auto-register from app/Console/Commands/
- **Middleware**: Configured in bootstrap/app.php
- **Queue**: Database driver (jobs, failed_jobs, job_batches)
- **Development Tools**: Laravel Boost v1.1, Pail (log viewer), Collision (error handling)
- **Code Quality**: Larastan v3.0, Pint v1.24
- **Testing**: Pest v4.1 with Laravel plugin v4.0

### Frontend
- **TailwindCSS v4**: @import syntax, CSS variables, no corePlugins
- **Vite**: Build tool with Laravel plugin
- **JavaScript**: ES6 modules, Axios setup
- **Font**: Instrument Sans

### Database Schema
- **users**: Standard auth table
- **cache/cache_locks**: Caching system
- **sessions**: Session management
- **jobs/failed_jobs/job_batches**: Queue system
- **migrations**: Migration tracking

# 🛠️ Development Patterns
## Code Style (Mandatory)
- **Strict Types**: Always `declare(strict_types=1)`
- **Type Hints**: Explicit return types and parameters
- **Constructors**: PHP 8 property promotion
- **Naming**: Descriptive (isRegisteredForDiscounts, not discount())
- **PHPDoc**: For complex logic, prefer inline for simple

## File Structure Patterns
- **Models**: Eloquent with casts() method
- **Controllers**: Form Request classes for validation
- **Routes**: Named routes with route() helper
- **Views**: Blade + TailwindCSS classes

## Testing Patterns
- **Framework**: Pest v4 syntax
- **Features**: Browser testing, smoke testing, visual regression
- **Assertions**: Specific methods (assertSuccessful, assertForbidden)
- **Mocking**: Pest\Laravel\mock() or $this->mock()

## Tools & Commands
- **Code Quality**:
  - `composer run code:check` - Check code style & static analysis
  - `composer run code:fix` - Fix code style & check static analysis
  - `composer run pint:dirty` - Fix only changed files
  - `composer run pint:check` - Check code style only
  - `composer run stan:check` - Run static analysis only
- **Laravel Boost**: search-docs, tinker, database-query, get-absolute-url
- **Testing**: Pest v4 features (browser, smoke, visual regression)
- **Development**: `composer run dev` - Run server, queue, and vite concurrently
- **Debugging**: Laravel Pail for log viewing

# 🧠 AI Memory Bank
## Critical Reminders
- ALWAYS search Laravel Boost docs before implementing features
- Use `composer run code:check` before committing any code changes
- Use `composer run code:fix` to automatically fix code style issues
- Use `composer run pint:dirty` for quick fixes on changed files only
- Update this file immediately when encountering new patterns or issues
- Follow Laravel 12 conventions strictly
- Test everything - write tests for all new functionality
- Use Laravel Boost tools (search-docs, tinker, database-query) for efficient development

## Lessons Learned
- Laravel 12: No Kernel.php, bootstrap/app.php handles everything
- TailwindCSS v4: @import syntax, no @tailwind directives
- Pest v4: Powerful browser testing capabilities available
- Laravel Boost v1.1: Integrated MCP tools for enhanced development
- Code Quality Scripts: Comprehensive pint & phpstan setup with CI-ready commands
- Concurrent Development: composer run dev for server + queue + vite
- Laravel Pail: Modern log viewer for debugging
- Collision: Enhanced error reporting and debugging

## AI Memory Bank - storing critically important knowledge