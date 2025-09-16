# Troubleshooting Guide

## Setup Issues

### Node.js Version Problems
```bash
# Use Node.js 20
nvm install 20
nvm use 20
```

### Package Installation Failures
```bash
# Clear npm cache
npm cache clean --force

# Delete node_modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

### TypeScript Compilation Errors
```bash
# Check TypeScript version
npx tsc --version

# Clear TypeScript build cache
npx tsc --build --clean
```

## Database Issues

### PostgreSQL Connection Problems
```bash
# Check if PostgreSQL is running
psql -h localhost -U postgres -d techflow_dev

# Reset database
npm run db:reset
```

### Migration Failures
```bash
# Check migration status
npm run db:migrate:status

# Rollback and retry
npm run db:migrate:rollback
npm run db:migrate
```

## Docker Issues

### Container Build Failures
```bash
# Clean Docker cache
docker system prune -a

# Rebuild without cache
docker-compose build --no-cache
```

### Port Conflicts
```bash
# Check what's using ports
lsof -i :3000
lsof -i :3001
lsof -i :5432

# Kill processes if needed
kill -9 <PID>
```

## Testing Issues

### Test Database Setup
```bash
# Create test database
createdb techflow_test

# Set test environment
export NODE_ENV=test
npm run test
```

### E2E Test Failures
```bash
# Install Playwright browsers
npx playwright install

# Run tests in headed mode for debugging
npx playwright test --headed
```

## Development Issues

### Hot Reload Not Working
```bash
# Clear Next.js cache
rm -rf .next

# Restart development server
npm run dev
```

### CORS Errors
Check your environment variables:
```bash
CORS_ORIGINS=http://localhost:3000,http://localhost:3002
```

## Deployment Issues

### Build Failures
```bash
# Check build locally
npm run build

# Check for TypeScript errors
npm run type-check
```

### Environment Variable Issues
Ensure all required environment variables are set:
```bash
# Check .env file
cat .env.example
```

## CI/CD Issues

### GitHub Actions Failures
1. Check the workflow logs in GitHub Actions tab
2. Ensure secrets are configured in repository settings
3. Verify workflow file syntax

### Security Scan Failures
```bash
# Fix security vulnerabilities
npm audit fix

# Check for high/critical vulnerabilities
npm audit --audit-level high
```

## Common Error Messages

### "Module not found"
- Check package.json dependencies
- Verify import paths
- Clear node_modules and reinstall

### "Cannot connect to database"
- Verify DATABASE_URL environment variable
- Check PostgreSQL service status
- Verify database exists

### "Permission denied"
- Check file permissions
- Verify Docker container user permissions
- Check database user permissions

## Getting Help

1. Check this troubleshooting guide first
2. Search existing GitHub Issues
3. Create a new GitHub Discussion with:
   - Error message
   - Steps to reproduce
   - Environment details (OS, Node version, etc.)
   - Relevant logs

## Debug Mode

Enable debug logging:
```bash
DEBUG=techflow:* npm run dev
```

For database queries:
```bash
DATABASE_LOGGING=true npm run dev
```