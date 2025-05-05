# ⚡ Ultra Wide Turbo Workspace 0.0.11

[![Brought to you by ultrawideturbodevs.com](https://img.shields.io/badge/Brought%20to%20you%20by-ultrawideturbodevs.com-blue?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0xIDE1aC0ydi0yaDJ2MnptMC00aC0yVjdoMnY2eiIvPjwvc3ZnPg==)](https://ultrawideturbodevs.com)

🎩 A virtual organization where you are the CEO. This workspace is structured around distinct **Roles**, each represented by a top-level folder acting as their dedicated "office".

---

## ✨ Latest Release: 0.0.10 (April 30, 2025)

#### 🛠️ Improvements
- Enhanced `generate_raycast_snippets-script.py` to run from the project root and correctly process files from prompts, templates, systems, and wows folders.

#### 🏗️ Infrastructure
- Added Raycast snippet generation capability: Creates JSON snippets from project markdown files with variable transformation support.

#### 🔄 Previous Release (0.0.9)
- Added standardized activity prompts (`plx-*.md`) across multiple roles (Architect, Business Analyst, Project Manager, Prompt Engineer).
- Refined the `project-manager` agent prompt with clearer instructions and a detailed PRD template.

#### 🛠️ Improvements
- Updated file counts and summaries in documentation.

#### 🔄 Previous Release (0.0.8)
- Restructured the project around top-level **Roles**, each with its own dedicated folder ("office").
- Standardized optional subfolders within roles: `prompts`, `templates`, `wows`, `rubrics`, `scripts`, `systems`.
- Rewritten `README.md` to accurately describe the new role-based structure and optional subfolders.
- Added a "Credits" section acknowledging `bmadcode` for influential repositories.
- Updated `CONTRIBUTING.md` to reflect the current file structure and remove outdated naming conventions.

---

## 📁 Role Folder Structure

Each role's top-level folder serves as their office. Inside, you can optionally organize resources into standardized subfolders to maintain consistency:

// TODO(GPT-AGENT): Add new folder 'snippets' - look at developer/snippets | 01/05/2025

| Folder                 | Purpose                                                                                                                                                                                                                                                                                                                                                                                                        | Examples                                                                                                       |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 💬 prompts/agents/     | An Agent Prompt is a structured instruction file (typically named you-are-{persona}.md) stored in a role's prompts/agents/ directory that defines an AI persona with specific expertise, responsibilities, and behaviors to guide AI interactions when assuming that role, providing the character traits, knowledge base, and workflow patterns needed to fulfill specialized functions within the workspace. | Files defining agent roles (e.g., `you-are-{persona}.md`)                                                      |
| 💬 prompts/activities/ | An Activity Prompt is a structured instruction file (typically named plx-*.md) that guides AI agents to perform specific, well-defined tasks within a role's domain, providing standardized formats and steps for completing discrete activities.                                                                                                                                                              | Files defining specific tasks (e.g., `plx-{activity}.md`)                                                      |
| 📋 templates/          | Standardized formats                                                                                                                                                                                                                                                                                                                                                                                           | Document templates, starter files (`*-template.md`)                                                            |
| ✨ wows/                | Way of Workings (Best Practices/Guides)                                                                                                                                                                                                                                                                                                                                                                        | How-to guides, tutorials, best practice docs (`wow-*.md`)                                                  |
| ✅ rubrics/             | Evaluation criteria                                                                                                                                                                                                                                                                                                                                                                                            | Quality standards, assessment frameworks (`*-rubric.md`)                                                       |
| 📜 scripts/            | Automated procedures                                                                                                                                                                                                                                                                                                                                                                                           | Shell scripts, Python scripts (`*-script.*`)                                                                   |
| ⚙️ systems/            | Repeatable workflows & standard procedures                                                                                                                                                                                                                                                                                                                                                                     | Process templates, defined workflows (`*-system.md`)                                                           |
| 📦 resources/          | Reusable assets & reference materials                                                                                                                                                                                                                                                                                                                                                                          | Collections of some kind, locations of specific tools, any other misc reusable inputs (`the-*.md`, `all-*.md`) |

---

## 👥 Roles

A role represents a specialized team member in your virtual organization with its own expertise, responsibilities, and dedicated workspace folder.

### 🏛️ [Architect](architect/) 
Creates detailed technical blueprints and architectural designs based on product requirements. Responsible for technology selection, standards definition, and making high-level design decisions.

```
architect/
├── prompts/ (7)
│   ├── activities/ (5)
│   └── agents/ (2)
└── templates/ (2)
```

### 📱 [ASO Expert](aso-expert/)
Specializes in App Store Optimization strategies to improve mobile application visibility, conversion rates, and ranking in app stores.

```
aso-expert/
├── prompts/ (1)
│   └── agents/ (1)
└── wows/ (1)
    └── best-practices/ (1)
```

### 📊 [Business Analyst](business-analyst/)
Performs market research and project definition, analyzing opportunities, competitors, and user demographics while creating structured project requirements.

```
business-analyst/
├── prompts/ (6)
│   ├── activities/ (3)
│   └── agents/ (3)
├── templates/ (1)
└── wows/ (1)
    └── best-practices/ (1)
```

### 📝 [Content Creator](content-creator/)
Develops optimized content for various platforms and channels, combining writing expertise with SEO knowledge to maximize engagement and reach.

```
content-creator/
├── prompts/ (5)
│   ├── activities/ (3)
│   └── agents/ (2)
├── resources/ (6)
│   └── dev-channels/ (6)
├── systems/ (3)
└── wows/ (1)
    └── best-practices/ (1)
```

### 💻 [Developer](developer/)
Implements features according to technical specifications, following coding standards and best practices while maintaining test coverage and documentation.

```
developer/
├── prompts/ (25)
│   ├── activities/ (16)
│   └── agents/ (9)
├── rubrics/ (1)
├── scripts/ (1)
├── templates/ (1)
└── wows/ (35)
    ├── astro/ (1)
    ├── cli-tools/ (2)
    ├── flutter/ (1)
    ├── markdown/ (1)
    ├── mcp-servers/ (2)
    ├── next-js/ (1)
    ├── open-source/ (1)
    └── supabase/ (26)
        ├── database/ (6)
        └── flutter/ (20)
```

### 📋 [Project Manager](project-manager/)
Creates product requirements documents and manages the Agile workflow of epics, stories, and tasks while coordinating development priorities.

```
project-manager/
├── prompts/ (18)
│   ├── activities/ (10)
│   └── agents/ (8)
├── templates/ (7)
└── wows/ (3)
```

### 🤖 [Prompt Engineer](prompt-engineer/)
Designs and optimizes prompts for AI interactions, creating standard formats for maintaining consistent development practices and agent behaviors.

```
prompt-engineer/
├── prompts/ (11)
│   ├── activities/ (7)
│   └── agents/ (4)
└── wows/ (4)
```

### 📑 [Proposal Manager](proposal-manager/)
Creates milestone proposals and project proposals that outline scope, requirements, and deliverables for stakeholder approval.

```
proposal-manager/
├── prompts/ (3)
│   ├── activities/ (1)
│   └── agents/ (2)
└── templates/ (1)
```

### 🧪 [Tester](tester/)
Designs and executes acceptance tests to validate functionality, ensure quality, and verify that requirements have been properly implemented.

```
tester/
├── prompts/ (3)
│   ├── activites/ (2)
│   └── agents/ (1)
└── templates/ (1)
```

### 🎨 [UI/UX Expert](uiux-expert/)
Translates UI/UX specifications into optimized designs and components, with expertise in creating intuitive user experiences and interfaces.

```
uiux-expert/
├── prompts/ (1)
│   └── agents/ (1)
└── rubrics/ (1)
```

---

## 🤝 Contributing

For detailed information on how to contribute to this project, please see the [CONTRIBUTING.md](CONTRIBUTING.md) file.
