# COPYRIGHT & HUMAN AUTHORSHIP GUIDANCE (AII Standard)

The AI Format Foundation recognizes that copyright protection for AI-assisted works requires meaningful human creative contribution. The AII Standard supports documentation of human authorship through structured metadata, provenance, and workflow history.

## 1. Human Authorship Requirements

An AI-generated image may be eligible for copyright if a human:
- Writes the prompts or textual descriptions
- Guides style, composition, lighting, color, or emotion
- Selects or rejects image outputs
- Edits, enhances, or refines the generated image
- Combines elements or adds human-created portions

Purely autonomous AI images with no human creative involvement are not copyrightable.

## 2. How AII Supports Copyright Claims

AII metadata captures:
- Creator identity (name, handle, email)
- Human-authored prompts and negative prompts
- Model and settings used
- Editing or post-processing decisions
- Timestamps and provenance trail

These fields help demonstrate meaningful human involvement in the creative process.

## 3. Recommended Manifest Fields for Legal Compliance

Creators may include these optional fields:

"human_authorship_statement": "I affirm that I contributed creative authorship...",
"human_signature": "Name or digital signature hash",
"creator_email": "email@example.com",
"editorial_notes": "Summary of human creative decisions."


## 4. Ownership

Copyright belongs to the human author(s) who contributed creative expression.  
If the work contains only unedited, uncurated AI output, it may not qualify for protection.

## 5. Licensing

Creators may include licensing information in `legal/license.txt` or related files.  
All distribution must follow applicable legal requirements.
