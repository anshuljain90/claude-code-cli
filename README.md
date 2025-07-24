# claude-code-cli
my personal tips to better use claude code

## Step 1: claude web

> Tip: use opus model for planning

- discuss your idea in detail with Claude web application or desktop app
- Discuss all product features
- tech stack, architecture, design decisions (or leave these up to Claude)
- once your are satisfied, paste below prompt/text in chat and it will help you generate `claude.md` file

```
# Claude Code Project Setup Prompt

Please create a comprehensive `claude.md` file for my software project that will be used by the Claude Code CLI tool. This file should serve as the complete project specification and guide for autonomous code generation.

## Project Context
I have discussed all requirements for a new product software and need you to create a structured markdown file that Claude Code can use to understand the project scope, requirements, and implementation details.

## Required claude.md Structure

Please create a `claude.md` file with the following sections:

### 1. Project Overview
- **Project Name**: [Specify the product name]
- **Description**: Brief summary of what the software does
- **Target Users**: Who will use this software
- **Core Value Proposition**: Main benefits and unique selling points

### 2. Technical Requirements
- **Technology Stack**: Frontend, backend, database, and any specific frameworks
- **Architecture Pattern**: Microservices, monolithic, serverless, etc.
- **Platform Targets**: Web, mobile, desktop, or combinations
- **Performance Requirements**: Expected load, response times, scalability needs
- **Security Requirements**: Authentication, authorization, data protection needs

### 3. Feature Specifications
- **Core Features**: Essential functionality (use user stories format)
- **Secondary Features**: Nice-to-have features
- **Integration Requirements**: Third-party APIs, external services
- **Admin Features**: Management, analytics, configuration needs

### 4. User Experience & Interface
- **User Journey**: Key user flows and interactions
- **UI/UX Requirements**: Design principles, accessibility needs
- **Responsive Design**: Device compatibility requirements
- **Branding Guidelines**: Color schemes, typography, visual identity

### 5. Data & Database Design
- **Data Models**: Key entities and relationships
- **Database Requirements**: Type, scalability, backup needs
- **API Specifications**: Endpoints, data formats, authentication
- **Data Privacy**: GDPR compliance, user data handling

### 6. Development Guidelines
- **Code Standards**: Coding conventions, naming patterns
- **Testing Strategy**: Unit, integration, e2e testing requirements
- **Documentation**: Code comments, API docs, user guides
- **Version Control**: Git workflow, branching strategy

### 7. Deployment & Operations
- **Hosting Requirements**: Cloud provider, infrastructure needs
- **CI/CD Pipeline**: Automated testing and deployment
- **Monitoring & Logging**: Error tracking, performance monitoring
- **Backup & Recovery**: Data backup strategy, disaster recovery

### 8. Project Constraints
- **Timeline**: Key milestones and deadlines
- **Budget Considerations**: Cost constraints or optimization needs
- **Compliance Requirements**: Legal, regulatory, or industry standards
- **Browser/Device Support**: Compatibility requirements

### 9. Success Metrics
- **KPIs**: Key performance indicators
- **User Metrics**: User engagement, retention goals
- **Technical Metrics**: Performance benchmarks, uptime targets
- **Business Metrics**: Revenue, conversion, growth targets

## Instructions for Claude Code

Based on our previous discussions about the product requirements, please:

1. **Analyze the Requirements**: Review all the features, technical specifications, and user needs we discussed
2. **Structure the Information**: Organize everything into the sections above with clear, actionable details
3. **Add Implementation Guidance**: Include specific technical decisions and implementation approaches
4. **Create User Stories**: Write detailed user stories for each feature using "As a [user type], I want [goal] so that [benefit]" format
5. **Define Acceptance Criteria**: For each feature, specify what constitutes completion
6. **Include Technical Specifications**: API endpoints, database schemas, component architecture
7. **Add Development Priorities**: Rank features by importance and development order

## Output Requirements

- Use clear, concise language that a developer can follow
- Include specific technical details, not just high-level concepts
- Provide enough context for Claude Code to make informed implementation decisions
- Structure content with proper markdown formatting for easy parsing
- Include code examples or pseudocode where helpful for clarity

Please create this `claude.md` file based on all the product requirements we've discussed, ensuring it's comprehensive enough for Claude Code to autonomously build the entire software product.
```


## Step 2: github

> Note: I am mentioning steps in context of github, you can ask any LLM to translate them for bitbucket

- create a new empty private (unless you want to explicitly want to make it public) repository
- go to [this link](https://github.com/settings/tokens) and creator token for your github account
- go to your local computer and clone YOUR repository using similar command

```
git clone https://anshuljain90:ghp_qgKfJh-LYaE45zU5kx79EQFQ-zJ8yj0L89nR@github.com/anshuljain90/claude-code-cli.git
```

- once you have empty repo/directory clonned on your local, download `cloud.md` file from claude web (generated in step1), rename if required but keep name as claude.md only

## Step 3: claude code cli

- install it
- cd into git repo root directory containing `claude.md` file
- run claude using command `claude` say yes each time asks ;)
- initialize claude code using command `init`
- change your default model to sonet using command `/config`
- now you can ask claude code to start writting the code and fix if anything do not work also ask it to create files like README.md, CHANGELOG.md, LICENSE.md, NOTICE.md etc. Example `create README.md, CHANGELOG.md, LICENSE.md, NOTICE.md files and start the implementation`

> Note: instead of `claude` to run the claude code, you can use `claude --permission-mode acceptEdits` or `claude --permission-mode acceptEdits --continue` or `claude --permission-mode bypassPermissions --continue` as well

## Sample files

 - [CHANGELOG.md](https://github.com/anshuljain90/claude-code-cli/blob/main/CHANGELOG.md)
 - [README.md](https://raw.githubusercontent.com/anshuljain90/claude-code-cli/refs/heads/main/README-SNIPPET.md)
