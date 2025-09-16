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

## AI-Assisted Development

### Q: Can I use GitHub Copilot, ChatGPT, or other AI tools?
**A**: **Absolutely yes!** We encourage the use of AI-assisted development tools including:
- GitHub Copilot
- ChatGPT/Claude
- Cursor/Windsurf
- Codeium
- Any other AI coding assistants

### Q: Will using AI tools affect my evaluation negatively?
**A**: No, AI usage will **not** negatively impact your evaluation. We're interested in the final code quality and your understanding of the implementation, not how you created it.

### Q: Do I need to document my AI usage?
**A**: While not required, we recommend documenting your AI tool usage in `docs/AI_USAGE.md`. This helps us understand your development process and can be valuable for discussion during technical interviews.

### Q: What if AI generates code I don't fully understand?
**A**: You must be able to explain all code in your solution during the technical interview. Take time to understand AI-generated code and modify it as needed to ensure it follows best practices.

### Q: Can AI help with architecture decisions?
**A**: Yes, but the final architectural decisions should be yours. Use AI for brainstorming and validation, but ensure you can justify your choices independently.

## Deployment & Infrastructure

### Q: Which cloud provider should I use?
**A**: You can use **any cloud or deployment platform** of your choice:
- **AWS** (recommended for enterprise experience)
- **Vercel** (excellent for Next.js)
- **Google Cloud Platform**
- **Microsoft Azure**
- **Railway, Render, Netlify** (simple deployment)
- **DigitalOcean, Heroku**
- **Self-hosted** solutions

### Q: Do I need to actually deploy the application?
**A**: Yes, a working live deployment accessible via URL is required. Choose a platform you're comfortable with.

### Q: Will deployment costs be covered?
**A**: We'll reimburse reasonable deployment costs up to $50 with receipts. Most platforms offer free tiers sufficient for this exam.

### Q: Can I use different platforms for different services?
**A**: Yes, you can deploy frontend and backend to different platforms if it makes sense for your architecture. Document your reasoning.

### Q: What if my chosen platform doesn't support certain features?
**A**: Document any platform limitations and explain how you would address them in a production environment.

## Technical Questions

### Q: Which database should I choose?
**A**: PostgreSQL is recommended for the relational data, but you can justify other choices based on your architecture needs.

### Q: Do I need to implement all authentication features?
**A**: Implement basic JWT authentication with role-based access control. Advanced features like 2FA are bonus points.

### Q: How should I handle multi-tenancy?
**A**: Document your approach (shared schema, separate schemas, or separate databases) and implement consistently.

### Q: What level of testing is expected?
**A**: Aim for 80% test coverage with a focus on business logic, API endpoints, and critical user flows.

### Q: Can I modify the GitHub Actions workflow?
**A**: Yes, you can customize the CI/CD pipeline to work with your chosen deployment platform. Document any changes you make.

## DevOps Questions

### Q: How complex should my CI/CD pipeline be?
**A**: Include code quality checks, testing, security scanning, and automated deployment to staging at minimum. Adapt to your chosen platform's capabilities.

### Q: Do I need Infrastructure as Code?
**A**: While recommended, you can use your platform's UI if needed. Document your infrastructure setup process either way.

### Q: What monitoring tools should I implement?
**A**: Use your platform's built-in monitoring where available. Additional monitoring tools are bonus points but not required.

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

### Q: How much time should I spend on deployment?
**A**: Plan for 2-3 hours on Day 2 for initial deployment setup. Use platforms with good developer experience to minimize deployment complexity.

## Evaluation

### Q: How is the exam evaluated?
**A**: See the detailed rubric in `docs/EVALUATION_RUBRIC.md`. Focus on code quality, system design, problem-solving, and DevOps skills.

### Q: Are there any automatic disqualifications?
**A**: Security vulnerabilities, completely non-functional code, or plagiarism will result in automatic failure.

### Q: Can I ask questions during the exam?
**A**: Use GitHub Discussions for clarifications. Responses are provided during business hours only.

### Q: Will my deployment platform choice affect my evaluation?
**A**: No, platform choice won't affect your score. We evaluate the quality of your deployment process and documentation, not the specific platform.

## Common Issues

### Q: My development environment isn't working
**A**: Check `TROUBLESHOOTING.md` for common setup issues. Use Docker if you're having environment problems.

### Q: Tests are failing in CI/CD
**A**: Ensure your tests work in a clean environment. Check database setup and environment variables.

### Q: Deployment is failing
**A**: Start with the simplest deployment strategy for your chosen platform. Complex infrastructure can be documented rather than implemented if time is limited.

### Q: My AI tool is suggesting conflicting approaches
**A**: Use your engineering judgment to choose the best approach. AI tools are assistants, not decision-makers. Document your reasoning for choosing one approach over another.

## Platform-Specific Tips

### Q: Best practices for Vercel deployment?
**A**: Use environment variables for configuration, optimize for static generation where possible, and leverage Vercel's built-in analytics.

### Q: AWS deployment complexity?
**A**: Start simple with Elastic Beanstalk or App Runner. Use more complex services like ECS only if you're comfortable with them.

### Q: Railway/Render best practices?
**A**: These platforms handle most infrastructure automatically. Focus on environment variable configuration and database setup.

### Q: Heroku limitations?
**A**: File system is ephemeral, so use cloud storage for file uploads. Document this limitation and how you'd address it in production.