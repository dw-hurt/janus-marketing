# ========================================
# DAILY WORKFLOW
# ========================================

# Check status (what changed?)
git status

# Add all changes
git add .

# Commit with message
git commit -m "Describe what you changed"

# Push to GitHub (backup)
git push origin main

# ========================================
# WORKING FROM ANOTHER COMPUTER
# ========================================

# First time: Clone
git clone https://github.com/dw-hurt/janus-marketing.git
cd janus-marketing

# Every time after: Pull latest
git pull origin main

# ========================================
# UNDOING MISTAKES
# ========================================

# Undo changes to a file (before commit)
git checkout -- filename.md

# Undo last commit (keep changes)
git reset --soft HEAD~1

# View history
git log --oneline

# ========================================
# VIEWING FILES
# ========================================

# List files
ls content\

# Read file
cat content\home-page-content.md

# Open in editor
code content\home-page-content.md

# ========================================
# BRANCHES (ADVANCED - FOR LATER)
# ========================================

# Create branch for experiments
git checkout -b new-feature

# Switch back to main
git checkout main

# Merge branch
git merge new-feature
YOUR COMPLETE WORKFLOW DIAGRAM
┌─────────────────────────────────────────────────────────┐
│  YOUR COMPUTER (Local Repository)                       │
│                                                          │
│  1. Create content files (Markdown)                     │
│     └─ content/home-page-content.md                     │
│                                                          │
│  2. Commit changes                                       │
│     git add . && git commit -m "message"                │
│                                                          │
│  3. Push to GitHub ──────────────────────┐              │
│     git push origin main                 │              │
└──────────────────────────────────────────┼──────────────┘
                                           │
                                           ▼
┌─────────────────────────────────────────────────────────┐
│  GITHUB (Remote Repository)                             │
│  https://github.com/dw-hurt/janus-marketing            │
│                                                          │
│  - Backup of all your files                             │
│  - Version history                                       │
│  - Accessible from anywhere                              │
│                                                          │
│  4. Pull from GitHub ◄───────────────┐                  │
│     git pull origin main             │                  │
└──────────────────────────────────────┼──────────────────┘
                                       │
                                       ▼
┌─────────────────────────────────────────────────────────┐
│  ANOTHER COMPUTER / PRODUCTION SERVER                    │
│                                                          │
│  5. Clone or Pull repository                             │
│     git clone <url> OR git pull                         │
│                                                          │
│  6. Build website using content files                    │
│     - Read content/*.md                                  │
│     - Convert to HTML in website/                        │
│     - Deploy website                                     │
└──────────────────────────────────────────────────────────┘
