[← Back to Claude-Prince2 Home](../../README.md)

# Design Decisions Record

## Project Evolution Context

### Phase 1: Embedded Coding Workflows
- AI-human collaboration for development
- Lifecycle management within single project context
- Workflow optimization for AI execution

### Phase 2: Claude-Swift (Deployable Operational System)  
- Portable template system with project hooks
- Single methodology deployment
- Router-subworkflow pattern established
- AI-optimized execution patterns proven

### Phase 3: Claude-PRINCE2 (First Methodology API)
- **Current Phase** - Create first 'API' version
- Prove methodology API concept
- Foundation for multi-methodology architecture

## Key Design Decisions

### Decision 1: Clone Claude-Swift as Foundation
**Decision:** Use claude-swift as starting point for claude-prince2
**Rationale:**
- Proven router-subworkflow infrastructure
- AI-optimized execution patterns established
- Audit system and session management battle-tested
- Focus energy on PRINCE2 content, not infrastructure rebuilding

### Decision 2: Methodology API Architecture
**Decision:** Transform claude-swift into PRINCE2-specific methodology API
**Future Vision:** Multiple methodology APIs coexisting (PRINCE2 + ITIL + others)
**Structure:**
```
project/claude/
├── prince2/     # PRINCE2 methodology API
├── itil/        # Future: ITIL methodology API  
└── shared/      # Cross-methodology coordination
```

### Decision 3: Retain Core Infrastructure
**Retained from Claude-Swift:**
- Router-subworkflow pattern → Methodology abstraction layer
- Audit logging system → Enhanced with PRINCE2 context
- Template deployment → Methodology API deployment
- AI-human collaboration patterns → Strategic-tactical partnership
- Session continuity → Project stage continuity

### Decision 4: PRINCE2 Alignment Strategy
**Approach:** Pragmatic PRINCE2 implementation (non-bureaucratic)
**Retain:** 7 Principles, 7 Themes, 7 Processes structure
**Simplify:** Lightweight documentation, flexible role assignments
**Optimize:** AI execution within PRINCE2 methodology constraints

### Decision 5: Step-by-Step Implementation
**Phase 1:** Core PRINCE2 workflows and data structures
**Phase 2:** Prove single methodology API concept  
**Phase 3:** Extract patterns for multi-methodology architecture
**Future:** Additional methodology APIs based on lessons learned

## Architectural Principles

### 1. AI-Optimized PRINCE2
- All workflows optimized for AI execution
- Human strategic control, AI tactical implementation
- PRINCE2 methodology constraints guide AI behavior

### 2. Router Pattern as Methodology Abstraction
- Top-level routers detect context and route to appropriate methodology
- Methodology-specific subworkflows optimized for their domain
- Clean separation enables parallel methodology development

### 3. Data Structure Alignment
- PRINCE2 management products as primary data structures
- Claude-swift audit enhanced with PRINCE2 context
- Template variables for project customization within PRINCE2 framework

### 4. Workflow Hierarchy
```
Level 1: Process Routers (initiate sesame, stage sesame, etc.)
Level 2: Theme Routers (risk sesame, quality sesame, etc.)
Level 3: Specific Subworkflows (create business case, authorize stage, etc.)
```

## Technical Decisions

### Workflow Triggers
- Retain sesame pattern from claude-swift
- Map to PRINCE2 processes and themes
- Examples: `initiate sesame`, `stage sesame`, `risk sesame`

### Data Structures
- PRINCE2 management products in structured directories
- Integration with existing audit system
- Role-based organization structure

### File Organization
```
prince2/
├── business-case/
├── plans/
├── registers/
├── reports/
└── controls/
```

## Success Criteria

### For Claude-PRINCE2 (Phase 1)
- Complete PRINCE2 methodology API working effectively  
- AI can execute PRINCE2 processes with human strategic guidance
- Proven template deployment of methodology API

### For Multi-Methodology Vision (Future)
- Multiple methodology APIs coexisting without conflict
- Cross-methodology coordination patterns established
- Scalable architecture for additional methodologies

## Next Steps

1. **Implement PRINCE2 analysis** - Complete top-level workflows identification
2. **Create core data structures** - PRINCE2 management products
3. **Transform existing workflows** - Map claude-swift workflows to PRINCE2 processes
4. **Test methodology API** - Validate single methodology approach
5. **Extract patterns** - Prepare for multi-methodology architecture

---

*This record captures the strategic decisions guiding the claude-swift to claude-prince2 transformation.*