# Project Setup Guide: Using AI Dev Tasks Workflow

This guide provides a step-by-step process for starting new projects using the AI Dev Tasks workflow. Follow this process to ensure consistent, structured development from idea to implementation.

## Prerequisites

- [Cursor](https://cursor.sh/) editor installed
- Access to the `ai-dev-tasks` repository (clone from your fork)
- Basic understanding of the target technology stack

## Step-by-Step Project Setup

### 1. Create New Project Directory

```bash
# Navigate to your projects directory
cd ~/projects

# Create new project directory
mkdir your-project-name
cd your-project-name

# Initialize git repository
git init
```

### 2. Copy AI Dev Tasks Files

```bash
# Copy the .mdc files from your ai-dev-tasks repository
cp ~/projects/ai-dev-tasks/*.mdc .

# Create tasks directory for PRDs and task lists
mkdir tasks
```

### 3. Create Initial Project Structure

For different project types, create the appropriate initial structure:

#### iOS App (Swift/SwiftUI)
```bash
# Create Xcode project using Xcode or command line
# File > New > Project > iOS > App
# Choose SwiftUI interface and Core Data if needed

# Create additional directories
mkdir docs
mkdir assets
mkdir tests
```

#### Web App (React/Next.js)
```bash
# Create Next.js app
npx create-next-app@latest . --typescript --tailwind --eslint --app

# Create additional directories
mkdir docs
mkdir components/ui
mkdir lib/utils
```

#### Backend API (Node.js/Express)
```bash
# Initialize npm project
npm init -y

# Install basic dependencies
npm install express cors helmet dotenv
npm install -D nodemon typescript @types/node

# Create directory structure
mkdir src
mkdir src/routes
mkdir src/middleware
mkdir src/models
mkdir docs
mkdir tests
```

### 4. Start the AI Dev Tasks Workflow

#### Phase 1: Create PRD
1. Open Cursor in your project directory
2. Start the Agent chat
3. Use the PRD creation command:

```text
Use @create-prd.mdc
Here's the feature/app I want to build: [Describe your project in detail]
```

4. Answer the clarifying questions thoroughly
5. Review and refine the generated PRD

#### Phase 2: Generate Task List
1. Once you have your PRD (e.g., `tasks/prd-your-feature.md`), generate tasks:

```text
Now take @tasks/prd-your-feature.md and create tasks using @generate-tasks.mdc
```

2. Review the high-level tasks
3. Respond with "Go" to generate detailed sub-tasks
4. Review the complete task list

#### Phase 3: Implementation
1. Start implementing tasks one by one:

```text
Please start on task 1.1 and use @task-list.mdc
```

2. Review each completed sub-task
3. Approve with "yes" or provide feedback
4. Continue until all tasks are complete

### 5. Project-Specific Setup

#### For iOS Projects
```bash
# Open Xcode project
open YourApp.xcodeproj

# Set up Core Data model if needed
# Configure app icons and launch screen
# Set up proper bundle identifier
```

#### For Web Projects
```bash
# Install additional dependencies as needed
npm install @radix-ui/react-icons lucide-react

# Set up environment variables
cp .env.example .env.local

# Start development server
npm run dev
```

#### For Backend Projects
```bash
# Set up environment variables
touch .env

# Create basic server structure
# Set up database connection
# Configure middleware
```

### 6. Version Control Setup

```bash
# Create appropriate .gitignore
# For iOS: Add Xcode-specific ignores
# For Node.js: Add node_modules, .env, etc.

# Make initial commit
git add .
git commit -m "Initial project setup with PRD and task list"

# Set up remote repository (optional)
git remote add origin https://github.com/yourusername/your-project.git
git push -u origin main
```

### 7. Documentation Setup

Create essential documentation files:

```bash
# Create README with project overview
touch README.md

# Create development setup instructions
touch DEVELOPMENT.md

# Create deployment guide
touch DEPLOYMENT.md
```

## Best Practices

### PRD Creation
- **Be Specific**: Provide detailed answers to clarifying questions
- **Think User-First**: Focus on user problems and benefits
- **Define Scope**: Clearly state what's in and out of scope
- **Consider Edge Cases**: Think about error conditions and unusual scenarios

### Task Generation
- **Review High-Level Tasks**: Ensure they make logical sense before generating sub-tasks
- **Break Down Complex Tasks**: If a task seems too large, ask the AI to break it down further
- **Prioritize Core Features**: Start with essential functionality before nice-to-haves

### Implementation
- **One Task at a Time**: Resist the urge to work on multiple tasks simultaneously
- **Test as You Go**: Verify each sub-task works before moving to the next
- **Document Decisions**: Keep notes on important technical decisions
- **Commit Frequently**: Make small, focused commits for each completed sub-task

### Code Quality
- **Follow Platform Conventions**: Use established patterns for your chosen technology
- **Write Tests**: Include unit tests for critical functionality
- **Handle Errors**: Implement proper error handling and user feedback
- **Optimize Performance**: Consider performance implications of implementation choices

## Technology-Specific Considerations

### iOS Development
- Use SwiftUI for modern iOS development
- Implement proper data persistence with Core Data
- Follow Apple's Human Interface Guidelines
- Test on multiple device sizes and iOS versions
- Consider accessibility from the start

### Web Development
- Use TypeScript for better code quality
- Implement responsive design principles
- Optimize for performance (Core Web Vitals)
- Consider SEO implications
- Test across different browsers

### Backend Development
- Design RESTful APIs with clear endpoints
- Implement proper authentication and authorization
- Use environment variables for configuration
- Set up proper logging and monitoring
- Design for scalability

## Troubleshooting

### Common Issues
- **AI Gets Stuck**: Break down the current task into smaller pieces
- **Requirements Unclear**: Go back to the PRD and add more detail
- **Technical Blockers**: Research the specific technology and update the task
- **Scope Creep**: Refer back to the PRD's non-goals section

### When to Iterate
- If the AI consistently struggles with tasks, the PRD might need more technical detail
- If requirements change significantly, update the PRD and regenerate tasks
- If you discover new technical constraints, document them and adjust the plan

## Example Project Structures

### iOS Recipe App
```
RecipeApp/
├── RecipeApp.xcodeproj
├── RecipeApp/
│   ├── App/
│   ├── Views/
│   ├── Models/
│   ├── ViewModels/
│   └── Resources/
├── tasks/
│   ├── prd-ios-recipe-app.md
│   └── tasks-prd-ios-recipe-app.md
├── docs/
├── README.md
└── .gitignore
```

### Web Dashboard
```
dashboard-app/
├── src/
│   ├── app/
│   ├── components/
│   ├── lib/
│   └── types/
├── tasks/
│   ├── prd-web-dashboard.md
│   └── tasks-prd-web-dashboard.md
├── docs/
├── package.json
├── README.md
└── .gitignore
```

## Conclusion

This workflow provides a structured approach to building features and applications with AI assistance. The key is to be thorough in the planning phase (PRD and tasks) and disciplined in the implementation phase (one task at a time).

Remember: The goal is not just to build software, but to build it systematically with clear documentation and verification at each step. 