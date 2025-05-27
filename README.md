# iOS Recipe App

A personalized cooking companion designed to make users more confident in their cooking by providing step-by-step guidance for creating great-tasting meals.

## Project Overview

This app solves the problem of recipe inflexibility by allowing users to customize recipes based on their specific needs at any given moment - whether that's adjusting for different ingredients, serving sizes, or cooking equipment.

**Goal**: Create the most flexible recipe app on the market, personalized to users' specific needs and designed to build a reliable rotation of perfectly replicatable meals.

## Key Features

- **Manual Recipe Entry**: Add recipes with detailed ingredients, portions, steps, and timing
- **Recipe Organization**: Folders, favorites, tags, and search functionality
- **Recipe Import**: Import from websites, links, apps, and photos
- **Customization**: Adjust serving sizes, substitute ingredients, modify equipment
- **Step-by-Step Cooking**: Guided cooking experience with individual step timing
- **Meal Planning**: Weekly meal planning and shopping list generation
- **Offline First**: Complete functionality without internet connectivity

## Technology Stack

- **Platform**: Native iOS (Swift/SwiftUI)
- **Data Persistence**: Core Data for local storage
- **UI Framework**: SwiftUI with dark mode optimization
- **Architecture**: MVVM pattern with local-first data approach

## Project Structure

```
ios-recipe-app/
├── RecipeApp.xcodeproj          # Xcode project (to be created)
├── RecipeApp/                   # Main app source code (to be created)
├── tasks/                       # AI Dev Tasks workflow files
│   └── prd-ios-recipe-app.md   # Product Requirements Document
├── docs/                        # Additional documentation
├── assets/                      # Design assets and resources
├── *.mdc                       # AI Dev Tasks command files
├── README.md                   # This file
└── .gitignore                  # Git ignore rules
```

## Development Workflow

This project uses the [AI Dev Tasks workflow](https://github.com/jmmlabs/ai-dev-tasks) for structured development:

1. ✅ **PRD Created**: Product Requirements Document completed
2. 🔄 **Next**: Generate task list using `@generate-tasks.mdc`
3. 🔄 **Then**: Implement tasks step-by-step using `@task-list.mdc`

## Getting Started

### Prerequisites

- Xcode 15.0 or later
- iOS 17.0 or later target
- macOS Ventura or later

### Setup Instructions

1. **Create Xcode Project**:
   - Open Xcode
   - File > New > Project
   - Choose iOS > App
   - Product Name: "RecipeApp"
   - Interface: SwiftUI
   - Language: Swift
   - Use Core Data: Yes
   - Include Tests: Yes

2. **Follow AI Dev Tasks Workflow**:
   ```text
   # In Cursor, generate task list from PRD
   Now take @tasks/prd-ios-recipe-app.md and create tasks using @generate-tasks.mdc
   
   # Then start implementation
   Please start on task 1.1 and use @task-list.mdc
   ```

3. **Development**:
   - Follow the generated task list step by step
   - Test each feature as it's implemented
   - Commit frequently with descriptive messages

## Design Philosophy

- **Clean & Minimalistic**: Focus on content without visual clutter
- **Dark Mode First**: Optimized for dark mode with light mode support
- **Kitchen-Friendly**: Large touch targets and spill-resistant navigation
- **Accessibility**: Full VoiceOver support for hands-free cooking

## Contributing

This is a personal project following the AI Dev Tasks methodology. The structured approach ensures:

- Clear requirements and scope
- Step-by-step implementation
- Verification at each stage
- Maintainable, well-documented code

## License

Private project - All rights reserved.

---

**Status**: 🚀 Project Setup Complete - Ready for task generation and implementation
