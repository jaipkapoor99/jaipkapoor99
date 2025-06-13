# The Mind: A Personal Knowledge Base for AI-Driven Self-Reflection

## Purpose of This Repository

This repository, "The Mind," serves as a structured personal knowledge base for Jai Kapoor. Its primary goal is to organize and consolidate a wide range of personal information, including memories, reflections, psychological assessments, and personal development plans, into a format optimized for analysis by Artificial Intelligence (AI) models.

The core objectives are:

1.  **AI-Enhanced Self-Understanding:** To leverage AI to gain deeper insights into personal psychological patterns, cognitive frameworks, emotional states, and developmental trajectories.
2.  **Structured Knowledge Organization:** To create a systematically organized digital archive of personal data that might otherwise be fragmented or inaccessible.
3.  **Facilitating Personal Growth:** By analyzing past experiences, therapeutic insights, and future aspirations, the aim is to support ongoing personal growth and self-improvement efforts.
4.  **Maximizing Informational Density for AI:** Files are intentionally processed to ensure each token (word or sub-word unit) carries maximum informational weight, prioritizing machine readability and analytical depth over conventional human readability for many of the source documents.

## Contents

The repository is structured into several key directories:

- **`Profile/`**: Contains synthesized profiles and high-level summaries intended for AI consumption, including a comprehensive AI profile and specific aspects like interests.

- **`Source/`**: Houses the raw and AI-optimized source materials, categorized into:

  - `Bio/`: Core biographical information and key relationships.
  - `Logs/`: Journals, logs, and reflective pieces.
  - `Therapy/`: Records related to psychological assessments, therapy, and rehabilitation.
  - `Interests/`: Personal interests and reflections on pop culture.
  - `Archive/`: Older or less frequently accessed documents.

- **`Projects/`**: Details on ongoing personal or professional projects.
- **`Plans/`**: Documents relating to personal goals, strategies, and plans.
- **`CP/`**: Contains information related to Competitive Programming.
- **`docs/`**: Documentation including workflow guides and entry templates.

## Automation and Workflow

This repository utilizes a highly automated workflow to ensure consistency, data integrity, and synchronization with external cloud services. The automation includes validation, profile generation, and cloud synchronization.

### Core Scripts

1.  **`scripts/master_script.py`**: The central automation hub that handles:

    - **Reference Validation**: Ensures all file references in `Profile/Index.txt` are valid
    - **Profile Generation**: Creates competitive programming profiles from Codeforces and LeetCode APIs
    - **File Concatenation**: Combines all `.txt` files into `concatenated_output.txt` for AI consumption
    - **Data Processing**: Manages the `Data_Dump.txt` staging file workflow
    - **Cloud Synchronization**: Syncs output to OneDrive and Google Drive
    - **GitHub Profile Sync**: Automatically updates GitHub profile repository with enhanced resume content

2.  **`scripts/validate_references.py`**: Validates repository integrity by:

    - Checking all file references in the index exist
    - Identifying unreferenced files (excluding system files)
    - Reporting broken references with detailed diagnostics

3.  **`scripts/commit_and_push.ps1`**: PowerShell orchestration script that:
    - Executes pre-commit validation and processing
    - Handles Git operations with user-provided commit messages
    - Triggers post-push cloud synchronization and GitHub profile updates

### Available Workflows

```bash
# Validate references only
py scripts/master_script.py validate

# Run pre-commit workflow (validation + processing)
py scripts/master_script.py pre-commit

# Run post-push workflow (cloud sync + GitHub profile sync)
py scripts/master_script.py post-push

# Update timestamp only
py scripts/master_script.py timestamp

# Run complete workflow
py scripts/master_script.py all
```

### Standard Commit Process

```powershell
# Run the complete commit and push workflow
.\scripts\commit_and_push.ps1 "Your commit message"
```

This process:

1. **Pre-Commit**: Validates references, generates profiles, concatenates files, clears staging
2. **Git Operations**: Commits with user message and pushes to remote
3. **Post-Push**: Syncs to cloud services (OneDrive and Google Drive) and updates GitHub profile

## Data Processing Methodology

### Information Flow

```
Raw Data (Data_Dump.txt) → Manual Organization → Structured Files → AI Input (concatenated_output.txt)
```

### Optimization Principles

- **AI Readability**: Hierarchical, keyword-focused formats
- **Token Density**: Maximum informational weight per word
- **Consistency**: Standardized entry templates and formats
- **Date Standardization**: YYYY-MM-DD format throughout
- **Reference Integrity**: Automated validation of all file references

### Entry Templates

The repository includes standardized templates for:

- Personal reflections and daily logs
- Memory documentation and analysis
- Therapy session notes
- Social interaction tracking
- Productivity and project work
- Recovery and meditation logs

See `docs/TEMPLATES.md` for detailed template specifications.

## Quality Assurance

### Automated Validation

- **Reference Checking**: Validates all file paths in the index
- **Error Handling**: Comprehensive error reporting and graceful degradation
- **Integrity Monitoring**: Detects missing files and broken references

### Error Recovery

- **Non-blocking Validation**: Workflows continue with warnings for non-critical issues
- **Detailed Diagnostics**: Clear error messages with actionable solutions
- **Backup Preservation**: Safe file operations with rollback capability

## Documentation

- **`docs/WORKFLOW.md`**: Comprehensive workflow documentation
- **`docs/TEMPLATES.md`**: Standardized entry templates
- **`CHANGELOG.md`**: Detailed change history
- **`README.md`**: This overview document

## Cloud Integration

### OneDrive Synchronization

- **Target**: `C:\Users\jaipk\OneDrive\Documents\AI\Therapy`
- **Content**: Complete concatenated output for AI analysis
- **Frequency**: Automatic after each successful push

### Google Drive Integration

- **Target**: NotebookLM folder for AI processing
- **Format**: Google Docs with full repository content
- **Authentication**: OAuth2 with persistent credentials

### GitHub Profile Integration

- **Target**: GitHub profile repository (`jaipkapoor99`)
- **Content**: Enhanced resume and professional showcase
- **Sync**: Automatic README.md synchronization with advanced C++ expertise
- **Features**: Professional profile with competitive programming achievements

## Resume and Professional Showcase

The repository includes comprehensive resume management:

- **`Profile/Resume.md`**: Markdown resume with enhanced C++ expertise
- **`Profile/Resume.txt`**: Text version synchronized from markdown
- **`Profile/Resume.html`**: Professional HTML version with custom styling
- **Automated Building**: Resume generation integrated into post-push workflow
- **Cloud Sync**: Resume HTML automatically synced to Google Drive
- **GitHub Profile**: Professional showcase automatically updated

## Security and Privacy

- **Credential Management**: Secure storage of API tokens
- **Data Sensitivity**: Awareness of personal information exposure
- **Access Control**: Proper file permissions and authentication

## Getting Started

1. **Clone the repository**
2. **Install Python dependencies** (see `scripts/master_script.py` for requirements)
3. **Configure cloud credentials** (OneDrive path, Google API credentials)
4. **Set up GitHub profile repository** (clone `jaipkapoor99` repository locally)
5. **Run validation**: `py scripts/master_script.py validate`
6. **Follow daily workflow**: Add data to `Data_Dump.txt` → Process → Commit

## Troubleshooting

Common issues and solutions are documented in `docs/WORKFLOW.md`. For immediate help:

1. **Validation Issues**: Check file paths and references
2. **API Failures**: Verify credentials and connectivity
3. **Cloud Sync Problems**: Validate authentication and permissions
4. **GitHub Profile Sync**: Ensure profile repository is cloned locally
5. **Resume Building**: Check pandoc installation and file permissions
6. **Script Errors**: Review error messages and check Python installation

This project represents an ongoing effort in personal data management and AI-assisted self-reflection, with a focus on systematic organization, automated processing, and comprehensive professional showcase integration.
