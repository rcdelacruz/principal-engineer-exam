# Principal Engineer 3-Day Coding Exam

## Overview
This exam evaluates a Principal Engineer candidate's ability to design, implement, and deploy a production-ready SaaS application with enterprise-grade considerations.

## Scenario
You're tasked with building **"TechFlow"** - a SaaS platform that combines:
- **E-commerce**: Product catalog and order management
- **Fintech**: Payment processing and financial reporting
- **Enterprise Tools**: Multi-tenant architecture with role-based access

## Evaluation Criteria
- **Code Quality & Architecture (35%)**: Clean code, design patterns, scalability
- **System Design Thinking (30%)**: Architecture decisions, trade-offs, documentation
- **Problem-solving Approach (20%)**: Creative solutions, edge case handling
- **DevOps/Deployment Skills (15%)**: CI/CD, security, monitoring

## Technology Stack
- **Frontend**: Next.js 14+ (App Router), TypeScript, Tailwind CSS
- **Backend**: Node.js with Express/Fastify, TypeScript
- **Database**: PostgreSQL (primary), Redis (caching)
- **Cloud**: AWS, GCP, Azure, or any cloud/deployment platform of your choice
- **CI/CD**: GitHub Actions (or your preferred CI/CD platform)
- **Additional**: Docker, ESLint, Prettier, Jest, Playwright

## AI-Assisted Development Policy

### ✅ **Allowed AI Tools**
You are **encouraged** to use AI-assisted development tools including:
- **GitHub Copilot** - Code completion and suggestions
- **ChatGPT/Claude** - Technical guidance and code review
- **Cursor/Windsurf** - AI-powered code editors
- **Codeium** - AI code completion
- **Any other AI coding assistants**

### 📋 **AI Usage Requirements**
1. **Document your AI usage** in your final submission
2. **Understand the code** - you must be able to explain all generated code
3. **Test AI-generated code** - ensure it works and follows best practices
4. **Customize AI suggestions** - don't blindly accept all suggestions

### 🎯 **Evaluation Approach**
- AI usage will **not** negatively impact your evaluation
- We evaluate **final code quality** and **your understanding**, not how you created it
- During technical interviews, you'll be asked to explain your implementation decisions

## Deployment Platform Flexibility

### ☁️ **Cloud Platform Options**
Deploy to **any platform** of your choice:
- **AWS** (recommended) - EC2, ECS, Lambda, Amplify
- **Google Cloud Platform** - Compute Engine, Cloud Run, App Engine
- **Microsoft Azure** - App Service, Container Instances, Functions
- **Vercel** - Excellent for Next.js applications
- **Netlify** - Good for frontend deployment
- **Railway** - Simple full-stack deployment
- **Render** - Easy deployment with databases
- **DigitalOcean** - App Platform or Droplets
- **Heroku** - Simple platform-as-a-service
- **Self-hosted** - Your own servers or VPS

### 📋 **Deployment Requirements**
1. **Working live deployment** accessible via URL
2. **Document your deployment process** in `docs/DEPLOYMENT.md`
3. **Include deployment automation** (CI/CD pipeline)
4. **Justify your platform choice** in your architecture documentation

### 💰 **Cost Considerations**
- Use **free tiers** when available
- We'll reimburse reasonable deployment costs (up to $50) with receipts
- Document estimated monthly costs for production scale

## Getting Started

1. **Fork this repository** to your personal GitHub account
2. **Clone your fork** and create a new branch for your work
3. **Read the detailed exam instructions** in `EXAM_INSTRUCTIONS.md`
4. **Choose your AI tools and deployment platform**
5. **Follow the day-by-day schedule** outlined in the instructions
6. **Submit your solution** by creating a pull request to your fork

## Quick Start Commands

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/principal-engineer-exam.git
cd principal-engineer-exam

# Install dependencies
npm install

# Set up development environment
npm run setup

# Start development servers
npm run dev
```

## Repository Structure

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
├── scripts/             # Build and utility scripts
└── .github/             # GitHub Actions workflows
```

## Submission Guidelines

### Required Deliverables
- Working application deployed to your chosen platform
- Complete documentation in `docs/` folder
- Comprehensive test suite with coverage report
- CI/CD pipeline configured and working
- Architecture documentation with diagrams

### Documentation Requirements
1. `docs/ARCHITECTURE.md` - System architecture and design decisions
2. `docs/API.md` - API documentation
3. `docs/DEPLOYMENT.md` - Deployment guide and platform choice justification
4. `docs/SCALING.md` - Scaling strategies and considerations
5. `docs/SECURITY.md` - Security measures and compliance
6. `docs/AI_USAGE.md` - Document how you used AI tools (optional but recommended)

### Code Quality Standards
- TypeScript strict mode enabled
- ESLint and Prettier configured
- Minimum 80% test coverage
- Conventional commit messages
- Clean git history with meaningful commits

## Evaluation Process

Your solution will be evaluated based on:

1. **Automated Checks** (GitHub Actions)
   - Code quality and linting
   - Type safety
   - Test coverage
   - Security scanning
   - Performance benchmarks

2. **Manual Review**
   - Architecture design quality
   - Problem-solving approach
   - Code organization and patterns
   - Documentation completeness
   - Deployment execution

3. **Technical Interview** (Optional)
   - Application walkthrough
   - Architecture explanation
   - Q&A about implementation decisions
   - AI tool usage discussion

## Time Allocation Guidelines

- **Day 1 (8 hours)**: Architecture design and foundation
- **Day 2 (8 hours)**: Implementation and DevOps setup  
- **Day 3 (8 hours)**: Testing, optimization, and documentation

## Support

- Check `docs/FAQ.md` for common questions
- Review `TROUBLESHOOTING.md` for setup issues
- Use GitHub Discussions for clarifications (monitored during business hours)

## Important Notes

- This is an individual assessment - do not collaborate with others
- **AI tools are encouraged** - use them to enhance your productivity
- **Any deployment platform is acceptable** - choose what you're comfortable with
- Document your decision-making process and trade-offs
- Focus on production readiness over feature completeness
- Quality over quantity - implement features thoroughly

## Platform-Specific Tips

### Vercel (Recommended for Next.js)
```bash
# Deploy with Vercel CLI
npm i -g vercel
vercel --prod
```

### AWS (Enterprise-grade)
- Use AWS CDK or Terraform for infrastructure
- Consider ECS Fargate for containers
- Use RDS for PostgreSQL and ElastiCache for Redis

### Railway (Simple full-stack)
- Connect GitHub repository
- Configure environment variables
- Automatic deployments on push

### Render (Database included)
- Easy PostgreSQL and Redis setup
- Web service deployment from GitHub
- Built-in SSL certificates

---

**Good luck! We're excited to see your solution and learn about your AI-assisted development process.**

## Contact

For urgent questions during the exam, contact: [your-email@company.com]