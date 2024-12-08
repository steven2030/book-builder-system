# Enhanced Book Builder Workflow

## Workflow Diagram

```mermaid
flowchart TD
    %% Initial Setup
    Start([Start]) --> Prompt[1. Create Dramatic Prompt]
    Prompt --> PlotSystem[2. Use Plot System]
    PlotSystem --> StoryOutline[3. Story Plot Outline]

    %% Document Generation
    StoryOutline --> GenDocs[4. Generate Documents]
    GenDocs --> ActDocs[Act Documents]
    GenDocs --> CharSheets[Character Sheets]

    %% Tracking Systems
    GenDocs --> CharArcs[5. Character Arcs Spreadsheet]
    CharArcs --> SubplotTracker[6. Subplot Tracker]

    %% Master Systems
    SubplotTracker --> MasterTracker[7. Master Tracker]
    MasterTracker --> AddInfo[8. Add Info to Master]

    %% Beat System Integration
    AddInfo --> Beats[9. Chapter Beats Development]
    
    %% Writing and Review
    Beats --> Improve[10. Review & Improve]
    Improve --> WriteChap[11. Write Chapter]
    WriteChap --> EditorCheck[12. Editor Review]
    
    %% Quality Control
    EditorCheck --> PhraseCheck[13. Check Repeat Phrases]
    PhraseCheck --> PlotReview[14. Review Against Plot]
    PlotReview --> Compile[15. Compile Chapters]

    %% Subprocesses
    subgraph "Master Tracker Details"
        MasterTracker --- MTColumns[Columns:<br/>- Chapter #<br/>- Act #<br/>- Tension Scale 1-10<br/>- Summary<br/>- Subplot Points<br/>- Timeline<br/>- Status]
    end

    subgraph "Editor Review System"
        EditorCheck --- ERSteps[Steps:<br/>- Style Check<br/>- Beat Alignment<br/>- Technical Accuracy<br/>- Character Consistency]
    end

    subgraph "Beat System"
        Beats --- BeatStruct[Structure:<br/>- Hook/Setup<br/>- Core Development<br/>- Cliffhanger/Bridge]
    end

    style Start fill:#f9f,stroke:#333,stroke-width:4px
    style MasterTracker fill:#bbf,stroke:#333,stroke-width:2px
    style EditorCheck fill:#bfb,stroke:#333,stroke-width:2px
    style Beats fill:#fbf,stroke:#333,stroke-width:2px
```

## Key Components

### 1. Initial Setup (Steps 1-3)
- Create dramatic premise
- Implement plot system
- Develop story outline

### 2. Documentation (Steps 4-6)
- Generate act documents
- Create character sheets
- Develop character arcs

### 3. Tracking Systems (Steps 7-8)
- Master tracker setup
- Information integration

### 4. Beat System (Step 9)
- Chapter beat development
- Three-part structure implementation

### 5. Writing & Review (Steps 10-12)
- Chapter development
- Editor review integration
- Quality checks

### 6. Quality Control (Steps 13-15)
- Phrase repetition check
- Plot alignment review
- Chapter compilation

## Usage Notes
1. Follow steps sequentially
2. Use integrated editor system throughout
3. Maintain consistent documentation
4. Update tracking systems regularly