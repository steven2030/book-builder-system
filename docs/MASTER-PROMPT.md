# Book Builder System - Master Prompt

## System Overview
This document contains the master prompts that drive the automated book building process using Claude. Each section corresponds to a step in the workflow diagram and includes the necessary prompts and validations.

## 1. Initial Setup Prompt

```markdown
You are a book building assistant. I need help creating a new book using the Book Builder System. Here are my initial details:

Book Title: [Title]
Genre: [Genre]
Target Length: [Length]
Key Themes: [Themes]

Please help me initialize the system by:
1. Creating the necessary GitHub repository structure
2. Setting up the master tracker
3. Preparing character sheets
4. Initializing subplot tracking
```

## 2. Master Tracker Setup

The master tracker spreadsheet contains:
- Chapter #
- Act #
- Rising tension scale (1-10)
- 3 line summary
- Subplot # integrations
- Timeline points
- Status

Prompt for tracker updates:
```markdown
Please update the master tracker with:
[New Information]

Ensure you:
1. Maintain consistent subplot numbering
2. Update tension scale appropriately
3. Verify timeline consistency
4. Cross-reference character involvement
```

## 3. Subplot Management

Subplot tracker contains:
- Subplot #
- Subplot summary
- Subplot opening
- Continuation points (1-3)
- Subplot end
- Character involvement
- Chapter integration points

Prompt for subplot creation/updates:
```markdown
I need to [create/update] subplot [#]:
Summary: [Brief description]
Characters involved: [Names]
Intended resolution: [Description]

Please help me:
1. Structure this subplot
2. Integrate it with the main plot
3. Track character involvement
4. Map chapter intersections
```

## 4. Character Arc Development

Character tracking includes:
- Character summary
- Arc overview
- Act 1 ARC
- Act 2 ARC
- Act 3 ARC
- Relationships
- Timeline points

Prompt for character development:
```markdown
For character [Name]:
Current Act: [1/2/3]
Development stage: [Description]
Key relationships: [Names]

Please:
1. Update character arc
2. Verify consistency with subplots
3. Track relationship developments
4. Maintain timeline accuracy
```

## 5. Integration and Validation

Regular check prompt:
```markdown
Please review current story state:
1. Verify subplot integration
2. Check character arc consistency
3. Validate timeline
4. Assess tension progression
5. Cross-reference all trackers
```

## Best Practices

1. Always maintain the rising tension scale accuracy
2. Cross-reference character involvement in each subplot
3. Regularly validate timeline consistency
4. Keep character arcs synchronized with main plot
5. Update all relevant trackers when adding new information

## Automation Notes

The system should:
- Automatically update related trackers when new information is added
- Maintain consistency across all documents
- Flag potential continuity issues
- Track subplot progression
- Monitor character development
- Validate timeline consistency

## Next Steps

After each prompt sequence:
1. Verify all trackers are updated
2. Cross-reference for consistency
3. Update GitHub documentation
4. Prepare next development phase