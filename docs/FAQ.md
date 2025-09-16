# Frequently Asked Questions

## General Questions

### Q: Can I use external libraries and frameworks?
**A**: Yes, you can use any open-source libraries and frameworks. Document your choices and reasoning in your architecture documentation.

### Q: How much should I implement vs. mock?
**A**: Focus on implementing core functionality thoroughly rather than building everything. It's better to have fewer features that are production-ready than many features that are half-finished.

### Q: Should I implement real payment processing?
**A**: Use Stripe's test mode or create a mock payment service. Do not use real payment credentials.

### Q: How detailed should my documentation be?
**A**: Documentation should be comprehensive enough for another senior engineer to understand your decisions and continue development.

## Technical Questions

### Q: Which database should I choose?
**A**: PostgreSQL is recommended for the relational data, but you can justify other choices based on your architecture needs.

### Q: Do I need to implement all authentication features?
**A**: Implement basic JWT authentication with role-based access control. Advanced features like 2FA are bonus points.

### Q: How should I handle multi-tenancy?
**A**: Document your approach (shared schema, separate schemas, or separate databases) and implement consistently.

### Q: What level of testing is expected?
**A**: Aim for 80% test coverage with a focus on business logic, API endpoints, and critical user flows.

## DevOps Questions

### Q: Which cloud provider should I use?
**A**: AWS is preferred, but GCP or Azure are acceptable. Choose based on your expertise and document your infrastructure decisions.

### Q: Do I need to actually deploy the application?
**A**: Yes, a working deployment is required. You can use free tiers of cloud providers.

### Q: How complex should my CI/CD pipeline be?
**A**: Include code quality checks, testing, security scanning, and automated deployment to staging at minimum.

## Time Management

### Q: What if I can't finish everything in 3 days?
**A**: Prioritize core functionality and production readiness over feature completeness. Document what you would implement with more time.

### Q: Can I work more than 8 hours per day?
**A**: The exam is designed for 8 hours per day. Quality is more important than working extra hours.

### Q: What should I focus on each day?
**A**: 
- Day 1: Architecture and foundation
- Day 2: Implementation and DevOps
- Day 3: Testing, optimization, and documentation

## Evaluation

### Q: How is the exam evaluated?
**A**: See the detailed rubric in `EVALUATION_RUBRIC.md`. Focus on code quality, system design, problem-solving, and DevOps skills.

### Q: Are there any automatic disqualifications?
**A**: Security vulnerabilities, completely non-functional code, or plagiarism will result in automatic failure.

### Q: Can I ask questions during the exam?
**A**: Use GitHub Discussions for clarifications. Responses are provided during business hours only.

## Common Issues

### Q: My development environment isn't working
**A**: Check `TROUBLESHOOTING.md` for common setup issues. Use Docker if you're having environment problems.

### Q: Tests are failing in CI/CD
**A**: Ensure your tests work in a clean environment. Check database setup and environment variables.

### Q: Deployment is failing
**A**: Start with a simple deployment strategy. Complex infrastructure can be documented rather than implemented if time is limited.