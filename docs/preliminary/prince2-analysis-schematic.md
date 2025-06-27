[← Back to Claude-Prince2 Home](../../README.md)

# PRINCE2 Analysis Schematic

## PRINCE2 Core Structure

### 7 Principles (Governance)
1. **Continued Business Justification** - Business case throughout
2. **Learn from Experience** - Lessons learned capture/apply
3. **Defined Roles & Responsibilities** - Clear accountability
4. **Manage by Stages** - Controlled progression
5. **Manage by Exception** - Escalation thresholds
6. **Focus on Products** - What gets delivered
7. **Tailor to Environment** - Adapt to project context

### 7 Themes (Management Areas)
1. **Business Case** - Why, value, justification
2. **Organization** - Roles, responsibilities, structure
3. **Quality** - Fitness for purpose criteria
4. **Plans** - How to achieve objectives
5. **Risk** - Uncertainty management
6. **Change** - Control modifications
7. **Progress** - Track, report, control

### 7 Processes (Workflow)
1. **Starting up a Project (SU)** - Pre-project preparation
2. **Directing a Project (DP)** - Project Board governance
3. **Initiating a Project (IP)** - Project setup
4. **Managing a Stage Boundary (SB)** - Stage transitions
5. **Controlling a Stage (CS)** - Stage execution
6. **Managing Product Delivery (MP)** - Work package delivery
7. **Closing a Project (CP)** - Project completion

## Top-Level Workflows (Sesame Triggers)

### Project Lifecycle Workflows
- `initiate sesame` → PROJECT_INITIATION (SU + IP processes)
- `stage sesame` → STAGE_MANAGEMENT (SB + CS processes)  
- `deliver sesame` → PRODUCT_DELIVERY (MP process)
- `close sesame` → PROJECT_CLOSURE (CP process)

### Theme Management Workflows
- `business sesame` → BUSINESS_CASE_MANAGEMENT (Theme 1)
- `risk sesame` → RISK_MANAGEMENT (Theme 5)
- `quality sesame` → QUALITY_MANAGEMENT (Theme 3)
- `change sesame` → CHANGE_MANAGEMENT (Theme 6)

### Governance Workflows
- `direct sesame` → PROJECT_DIRECTION (DP process)
- `report sesame` → PROGRESS_REPORTING (Theme 7)
- `exception sesame` → EXCEPTION_MANAGEMENT (Principle 5)

## Core Data Structures

### Management Products (Documents)
```
prince2/
├── business-case/
│   ├── business-case.md
│   └── benefits-review-plan.md
├── plans/
│   ├── project-plan.md
│   ├── stage-plans/
│   └── team-plans/
├── registers/
│   ├── risk-register.md
│   ├── issue-register.md
│   ├── quality-register.md
│   └── lessons-log.md
├── reports/
│   ├── highlight-reports/
│   ├── checkpoint-reports/
│   └── end-stage-reports/
└── controls/
    ├── project-initiation-document.md
    ├── work-packages/
    └── stage-boundaries/
```

### Audit Integration
**Retain claude-swift audit with PRINCE2 extensions:**
```
TIMESTAMP|WORKFLOW|STEP_TYPE|CONTEXT|FILE_PATH|DESCRIPTION
TIMESTAMP|PRINCE2_STAGE|stage_boundary|initiation|prince2/controls/stage-boundaries/initiation-boundary.md|Stage boundary approved
TIMESTAMP|RISK_MANAGEMENT|risk_identified|technical|prince2/registers/risk-register.md|New technical risk added
TIMESTAMP|BUSINESS_CASE|justification_review|quarterly|prince2/business-case/business-case.md|Business case reviewed and updated
```

### Role Structure
```
organization/
├── project-board/
│   ├── executive.md
│   ├── senior-user.md
│   └── senior-supplier.md
├── project-manager/
│   └── project-manager.md
└── teams/
    ├── team-managers/
    └── specialists/
```

## Workflow Hierarchy

### Level 1: Process Routers
- **PROJECT_INITIATION** → Routes to SU/IP subworkflows
- **STAGE_MANAGEMENT** → Routes to SB/CS subworkflows
- **PRODUCT_DELIVERY** → Routes to MP subworkflows

### Level 2: Theme Routers  
- **BUSINESS_CASE_MANAGEMENT** → Routes to business case subworkflows
- **RISK_MANAGEMENT** → Routes to risk theme subworkflows
- **QUALITY_MANAGEMENT** → Routes to quality theme subworkflows

### Level 3: Specific Subworkflows
- **CREATE_BUSINESS_CASE** (IP subworkflow)
- **AUTHORIZE_STAGE** (SB subworkflow)
- **CAPTURE_LESSONS** (All processes)
- **ESCALATE_EXCEPTION** (CS subworkflow)

## Integration Points

### Claude-Swift Retained Components
- **Audit system** → Enhanced with PRINCE2 context
- **Session management** → Project stage continuity
- **Template deployment** → PRINCE2 methodology API
- **Router-subworkflow pattern** → PRINCE2 process navigation

### PRINCE2-Specific Additions
- **Stage gates** → Formal approval workflows
- **Product registers** → Deliverable tracking
- **Exception handling** → Escalation procedures
- **Lessons learned** → Experience capture/application

## Data Flow Patterns

### Project Progression
```
Business Case → Project Plan → Stage Plans → Work Packages → Products
     ↓              ↓             ↓             ↓           ↓
Risk Register → Risk Actions → Risk Reviews → Risk Updates → Risk Closure
```

### Control Flow
```
Stage Boundary → Go/No-Go Decision → Next Stage Authorization → Stage Execution
       ↑                 ↓                       ↓                    ↓
Exception Reports ← Progress Reports ← Checkpoint Reports ← Work Package Reports
```

## Implementation Strategy

### Phase 1: Core Processes
1. **PROJECT_INITIATION** workflow with business case
2. **STAGE_MANAGEMENT** workflow with stage boundaries
3. **Basic registers** (risk, issue, quality)

### Phase 2: Theme Integration
1. **RISK_MANAGEMENT** workflow with risk theme
2. **QUALITY_MANAGEMENT** workflow with quality theme
3. **CHANGE_MANAGEMENT** workflow with change theme

### Phase 3: Governance Layer
1. **PROJECT_DIRECTION** workflow for Project Board
2. **EXCEPTION_MANAGEMENT** workflow for escalations
3. **LESSONS_LEARNED** workflow for experience capture

---

*This schematic provides the foundation for transforming claude-swift into claude-prince2 methodology API.*