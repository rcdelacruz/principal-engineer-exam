# Principal Engineer 3-Day Coding Exam - Detailed Instructions

## Overview
This exam evaluates a Principal Engineer candidate's ability to design, implement, and deploy a production-ready SaaS application with enterprise-grade considerations.

## Scenario
You're tasked with building **"TechFlow"** - a SaaS platform that combines:
- **E-commerce**: Product catalog and order management
- **Fintech**: Payment processing and financial reporting
- **Enterprise Tools**: Multi-tenant architecture with role-based access

---

# Day 1: Architecture & Foundation (8 hours)

## Morning (4 hours): System Design & Architecture

### Task 1.1: Architecture Document (2 hours)
Create a comprehensive architecture document covering:

1. **System Overview**
   - High-level architecture diagram
   - Component interactions
   - Data flow diagrams

2. **Technical Decisions**
   - Database schema design (multi-tenant)
   - API design (REST/GraphQL choice)
   - Authentication/Authorization strategy
   - Caching strategy
   - File storage approach

3. **Scalability Considerations**
   - Horizontal scaling approach
   - Database sharding strategy
   - CDN integration
   - Load balancing

4. **Security Architecture**
   - Data encryption (at rest/in transit)
   - PCI DSS compliance considerations
   - Rate limiting strategy
   - Input validation approach

**Deliverable**: `docs/ARCHITECTURE.md`

### Task 1.2: Database Design (2 hours)
Design and implement database schemas:

1. **Multi-tenant Schema**
   ```sql
   -- Organizations (tenants)
   -- Users with role-based access
   -- Products with categories
   -- Orders and payments
   -- Audit logs
   ```

2. **Migration Strategy**
   - Create migration files
   - Seed data for testing
   - Rollback procedures

3. **Performance Optimization**
   - Index strategy
   - Query optimization
   - Connection pooling

**Deliverables**: 
- `packages/database/migrations/`
- `packages/database/seeds/`
- `docs/DATABASE.md`

## Afternoon (4 hours): Project Setup & Core Backend

### Task 1.3: Project Structure & Configuration (1 hour)
Set up the complete project structure:

```
techflow/
├── apps/
│   ├── web/              # Next.js frontend
│   ├── api/              # Express/Fastify API
│   └── admin/            # Admin dashboard
├── packages/
│   ├── database/         # Database schemas & migrations
│   ├── shared/           # Shared types & utilities
│   ├── auth/            # Authentication library
│   └── ui/              # Shared UI components
├── infrastructure/       # IaC and deployment configs
├── docs/                # Documentation
└── scripts/             # Build and utility scripts
```

### Task 1.4: Core Backend Implementation (3 hours)

1. **Authentication Service**
   - JWT-based authentication
   - Role-based authorization
   - Multi-tenant context switching
   - Password reset flow

2. **Core API Endpoints**
   ```typescript
   // Organizations
   POST /api/v1/organizations
   GET /api/v1/organizations/:id
   
   // Products
   GET /api/v1/products
   POST /api/v1/products
   PUT /api/v1/products/:id
   
   // Orders
   POST /api/v1/orders
   GET /api/v1/orders/:id
   PUT /api/v1/orders/:id/status
   
   // Payments
   POST /api/v1/payments/process
   GET /api/v1/payments/:id
   ```

3. **Middleware Implementation**
   - Request validation
   - Rate limiting
   - Audit logging
   - Error handling

**Deliverables**:
- Working API with core endpoints
- Authentication middleware
- Input validation schemas
- Error handling system

---

# Day 2: Advanced Implementation & DevOps (8 hours)

## Morning (4 hours): Frontend & Integration

### Task 2.1: Next.js Application (3 hours)

1. **App Architecture**
   - Server components vs client components strategy
   - Layout structure with navigation
   - Route groups for different user types

2. **Key Pages Implementation**
   ```typescript
   // Public pages
   /login, /register, /pricing
   
   // Dashboard pages (role-based)
   /dashboard/products
   /dashboard/orders
   /dashboard/analytics
   /dashboard/settings
   
   // Admin pages
   /admin/organizations
   /admin/users
   /admin/system-health
   ```

3. **State Management**
   - Server state with React Query/SWR
   - Client state with Zustand/Context
   - Form handling with React Hook Form

4. **UI Components**
   - Reusable component library
   - Responsive design
   - Accessibility considerations

### Task 2.2: Payment Integration (1 hour)
Implement payment processing:
- Stripe/PayPal integration
- Webhook handling for payment status
- PCI-compliant card storage approach
- Refund processing

## Afternoon (4 hours): DevOps & Deployment

### Task 2.3: CI/CD Pipeline (2 hours)

1. **GitHub Actions Workflows**
   ```yaml
   # .github/workflows/ci.yml
   # - Code quality checks (ESLint, Prettier)
   # - Type checking
   # - Unit tests
   # - Integration tests
   # - Security scanning
   # - Build verification
   
   # .github/workflows/cd.yml
   # - Automated deployment to staging
   # - Production deployment (manual approval)
   # - Database migrations
   # - Health checks
   # - Rollback procedures
   ```

2. **Quality Gates**
   - Code coverage minimum (80%)
   - Performance budget checks
   - Security vulnerability scanning
   - Bundle size monitoring

### Task 2.4: Infrastructure as Code (2 hours)

1. **Docker Configuration**
   ```dockerfile
   # Multi-stage builds for optimization
   # Development and production variants
   # Health checks
   # Security best practices
   ```

2. **AWS Infrastructure** (choose one approach)
   - **CDK/Terraform**: Complete infrastructure definition
   - **Docker Compose**: Local development environment
   - **Kubernetes**: Manifests for container orchestration

3. **Monitoring & Observability**
   - Application metrics (Prometheus/CloudWatch)
   - Logging strategy (structured logs)
   - Health check endpoints
   - Error tracking (Sentry integration)

**Deliverables**:
- Complete CI/CD pipeline
- Infrastructure automation
- Monitoring setup
- Deployment documentation

---

# Day 3: Optimization & Production Readiness (8 hours)

## Morning (4 hours): Performance & Testing

### Task 3.1: Performance Optimization (2 hours)

1. **Frontend Performance**
   - Code splitting and lazy loading
   - Image optimization
   - Caching strategies
   - Core Web Vitals optimization

2. **Backend Performance**
   - Database query optimization
   - Redis caching implementation
   - API response optimization
   - Connection pooling

3. **Performance Monitoring**
   - Lighthouse CI integration
   - Application performance monitoring
   - Database performance metrics

### Task 3.2: Comprehensive Testing (2 hours)

1. **Test Pyramid Implementation**
   ```typescript
   // Unit tests (70%)
   // Integration tests (20%)
   // E2E tests (10%)
   ```

2. **Test Coverage**
   - Core business logic
   - API endpoints
   - Authentication flows
   - Payment processing
   - Error scenarios

3. **Test Automation**
   - Playwright for E2E testing
   - API testing with Supertest
   - Database testing strategies
   - Mock strategies for external services

## Afternoon (4 hours): Security & Scalability

### Task 3.3: Security Implementation (2 hours)

1. **Security Hardening**
   - Input sanitization and validation
   - SQL injection prevention
   - XSS protection
   - CSRF protection
   - Rate limiting per user/IP

2. **Data Protection**
   - PII data encryption
   - Secure session management
   - API key management
   - Environment variable security

3. **Compliance Considerations**
   - GDPR compliance features
   - Data retention policies
   - Audit trail implementation
   - Right to be forgotten

### Task 3.4: Scalability & Resilience (2 hours)

1. **Scaling Strategy**
   - Horizontal scaling plan
   - Database read replicas
   - Microservices migration path
   - Event-driven architecture considerations

2. **Resilience Patterns**
   - Circuit breaker implementation
   - Retry mechanisms with exponential backoff
   - Graceful degradation
   - Fallback strategies

3. **Operational Excellence**
   - Health check endpoints
   - Metrics and alerting
   - Log aggregation
   - Incident response procedures

**Final Deliverables**:
- Production-ready application
- Comprehensive test suite
- Security audit report
- Scaling documentation
- Operational runbook

---

# Submission Requirements

## Code Quality Expectations
- **TypeScript**: Strict mode, proper typing
- **Code Style**: ESLint + Prettier configuration
- **Documentation**: JSDoc for complex functions
- **Git**: Conventional commits, meaningful history

## Documentation Required
1. `README.md` - Setup and running instructions
2. `docs/ARCHITECTURE.md` - System architecture
3. `docs/API.md` - API documentation
4. `docs/DEPLOYMENT.md` - Deployment guide
5. `docs/SCALING.md` - Scaling considerations
6. `docs/SECURITY.md` - Security measures

## Deployment Verification
The application should be deployable and demonstrate:
- Multi-tenant functionality
- Payment processing (test mode)
- Role-based access control
- Real-time features (if implemented)
- Performance under load

## Evaluation Criteria Details

### Code Quality & Architecture (35%)
- Clean, maintainable code structure
- Proper separation of concerns
- Design pattern implementation
- TypeScript usage and type safety
- Error handling and edge cases

### System Design Thinking (30%)
- Architecture documentation quality
- Database design decisions
- Scalability considerations
- Technology choice justifications
- Trade-off analysis

### Problem-solving Approach (20%)
- Creative solution implementation
- Edge case handling
- Performance optimization
- User experience considerations
- Business logic implementation

### DevOps/Deployment Skills (15%)
- CI/CD pipeline effectiveness
- Infrastructure automation
- Security implementation
- Monitoring and observability
- Documentation quality

---

# Bonus Challenges (Optional)

If time permits, candidates can implement:

1. **Real-time Features**
   - WebSocket implementation for order updates
   - Real-time inventory management
   - Live chat support system

2. **Advanced Analytics**
   - Revenue reporting dashboard
   - User behavior analytics
   - Performance metrics visualization

3. **Mobile Considerations**
   - PWA implementation
   - Mobile-responsive design
   - Push notification system

4. **Advanced Security**
   - Two-factor authentication
   - Single sign-on (SSO) integration
   - Advanced rate limiting

---

# Time Management Tips

## Day 1 Focus
- Spend adequate time on architecture decisions
- Don't over-engineer the initial implementation
- Focus on core functionality first

## Day 2 Focus
- Prioritize working deployment over perfect code
- Ensure CI/CD pipeline works end-to-end
- Test deployment early and often

## Day 3 Focus
- Focus on production readiness
- Implement monitoring and alerting
- Document operational procedures
- Ensure security best practices

## General Tips
- Commit frequently with meaningful messages
- Document decisions and trade-offs
- Test early and continuously
- Consider the evaluator's perspective when documenting