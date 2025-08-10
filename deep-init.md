# CLAUDE.md Generation Prompt

Use this prompt to systematically generate comprehensive CLAUDE.md documentation for any project. This creates a complete documentation set that helps Claude Code understand and work effectively with the codebase.

---

# Generate Complete CLAUDE.md Documentation Set

I need you to create a comprehensive set of CLAUDE.md files for this project using the systematic approach below. Work through each phase methodically to ensure high-quality, consistent documentation.

## Phase 1: Project Discovery & Analysis

### Step 1: Discover Project Structure
1. **Map all directories** (including hidden directories like `.scripts`, `.github`, etc.)
   - Use: `find . -type d -name ".*" -o -type d -not -path "*/.*" | head -20`
   - Use: `LS` tool to explore key directories
   
2. **Filter git-ignored directories**
   - Read `.gitignore` file if it exists
   - Exclude common ignore patterns: `node_modules`, `dist`, `build`, `target`, `.git`, etc.
   - Focus on directories that contain source code, configuration, or infrastructure

3. **Analyze project type and technology stack**
   - Examine root files: `package.json`, `Cargo.toml`, `setup.py`, `Makefile`, etc.
   - Identify primary programming languages
   - Note build tools, test frameworks, CI/CD systems

### Step 2: Classify Directories by Purpose
For each directory, determine its category:

- **Core/Source**: Main application code, libraries, modules
- **Configuration/Resources**: Config files, templates, static resources  
- **Testing**: Test files, test utilities, test fixtures
- **Build/CI**: Build scripts, CI/CD workflows, containerization
- **Documentation**: Docs, examples, guides
- **Tools/Scripts**: Utility scripts, development tools
- **Infrastructure**: Deployment, monitoring, infrastructure-as-code

### Step 3: Map Integration Relationships  
Identify how directories connect:
- Which directories depend on others?
- What are the data/control flow relationships?
- How do build/test processes connect components?
- What external integrations exist?

## Phase 2: Generate Directory-Specific CLAUDE.md Files

For each significant directory (skip trivial single-file directories), create a CLAUDE.md file using this approach:

### Directory Analysis Template
Before writing each CLAUDE.md, analyze:
1. **What files are in this directory?** (use `LS` tool)
2. **What is the directory's primary purpose?**  
3. **How does it integrate with other parts of the project?**
4. **What external dependencies does it have?**
5. **What would a developer need to know to modify this directory?**

### CLAUDE.md Generation Process
1. **Use the CLAUDE-template.md** as your structural guide
2. **Choose appropriate sections** based on directory type:
   - **Executable/Scripts**: Core Functions, Entry Point, Usage Patterns
   - **Resources/Config**: Core Files & Architecture, File Relationships
   - **Testing**: Testing Framework, Test Structure, Build System Integration
   - **CI/CD**: Workflow Architecture, Supporting Infrastructure, Development Practices
   - **Documentation**: Content Organization, Build Process, Usage Guidelines

3. **Generate meaningful content** by:
   - Reading key files in the directory to understand functionality
   - Analyzing file patterns and naming conventions
   - Understanding the technology stack used
   - Identifying the directory's role in the overall system

4. **Ensure Integration Points section** describes:
   - Connections to other project directories
   - Build system integration
   - External tool dependencies
   - CI/CD pipeline involvement

### Required Quality Standards
- **Specific, not generic**: Content should reflect actual directory contents
- **Technically accurate**: Based on actual file analysis, not assumptions  
- **Useful for development**: Include information Claude Code needs to modify/extend
- **Consistent formatting**: Follow template structure and formatting standards
- **Proper cross-references**: Link to related directories and files explicitly

## Phase 3: Generate Root CLAUDE.md Overview

Create a comprehensive root `CLAUDE.md` that includes:

### Required Sections for Root File

1. **Project Overview**
   - What the project does (based on README, package files, etc.)
   - Key technologies and architecture approach
   - Primary use cases or target users

2. **Core Architecture**  
   - Directory structure overview with brief descriptions
   - Major component relationships
   - Data flow and control flow patterns
   - Key architectural decisions

3. **Development Commands**
   - Build commands (from Makefile, package.json, etc.)
   - Test execution (local and CI approaches)
   - Development workflow commands
   - Deployment/release processes

4. **Integration Points**
   - How components connect and depend on each other
   - External service integrations
   - Build tool chain integration
   - CI/CD pipeline overview

5. **Dependencies & Requirements**
   - Runtime dependencies
   - Development tool requirements
   - System/platform requirements
   - Installation prerequisites

### Root File Quality Standards
- **Comprehensive but focused**: Cover all major aspects without overwhelming detail
- **Developer-oriented**: Emphasize information needed for effective development
- **Cross-reference rich**: Link to relevant directory-specific CLAUDE.md files
- **Workflow-focused**: Include common development scenarios and approaches

## Phase 4: Validation & Consistency Check

### Final Review Checklist
1. **Completeness**: CLAUDE.md exists for all significant directories
2. **Consistency**: All files follow template structure and formatting
3. **Accuracy**: Content reflects actual directory contents and project structure  
4. **Integration**: Cross-references between files are accurate and helpful
5. **Usefulness**: Documentation provides actionable information for development work

### Common Issues to Avoid
- **Generic template filling**: Content should be specific to actual directory purpose
- **Missing cross-references**: Files should reference related components appropriately
- **Inconsistent terminology**: Use same terms for same concepts across all files
- **Outdated information**: Ensure content reflects current directory state
- **Missing integration context**: Each directory's role in the system should be clear

## Execution Instructions

1. **Start with Phase 1** - Complete project discovery before generating any files
2. **Work systematically** - Generate directory files before root overview
3. **Use actual file analysis** - Read files to understand purpose, don't guess
4. **Maintain consistency** - Use established patterns and terminology throughout
5. **Cross-reference appropriately** - Ensure files link to related components
6. **Validate comprehensiveness** - Ensure all significant directories are documented

The goal is creating a complete documentation set that makes Claude Code maximally effective when working with the project, following the proven patterns established in the CLAUDE-template.md.

---

## Usage Notes

**When to use this prompt:**
- New projects that need comprehensive CLAUDE.md documentation
- Existing projects lacking consistent documentation
- Projects where directory structure has evolved significantly
- When establishing documentation standards for a team

**Adaptation for specific projects:**
- Modify directory classification based on project type
- Add project-specific sections as needed
- Adjust technical depth based on project complexity
- Include project-specific development workflows

**Quality indicators:**
- Each CLAUDE.md provides clear, actionable information
- Cross-references help navigate between related components  
- Documentation accurately reflects current project state
- Files follow consistent structure and formatting
- Root overview provides effective project onboarding for Claude Code
