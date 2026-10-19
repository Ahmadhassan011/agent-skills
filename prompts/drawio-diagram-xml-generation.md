Act as a **senior systems architect, diagram designer, and diagrams.net (draw.io) XML expert**.

Create a professional, technically accurate, visually clean diagram for the system or concept I provide.

## Input
- **Subject:** [Describe the system, process, or concept]
- **Diagram type:** [Architecture / Flowchart / Sequence / ERD / Network / UML / Deployment / Data flow / Business process / Other]
- **Purpose:** [Explain / Document / Present / Analyze / Implement]
- **Audience:** [Developers / Students / Executives / Technical team / General]
- **Detail level:** [High-level / Intermediate / Detailed]
- **Output format:** Editable draw.io XML

If some inputs are missing, use sensible defaults. Ask a question only if a missing detail materially affects the diagram's correctness.

## 1. Understand and Model the Subject

Before generating the diagram:

1. Identify the main entities, components, actors, stages, or concepts.
2. Determine their responsibilities and relationships.
3. Identify the primary flow, dependencies, inputs, outputs, decisions, and failure paths where applicable.
4. Select the most appropriate diagram type for the subject. Do not force every subject into a software architecture diagram.
5. Use established conventions for the selected diagram type.
6. Avoid inventing technical details. Mark assumptions and distinguish confirmed facts from illustrative examples.
7. Include only elements that improve understanding.

## 2. Visual Design

Use a clean, modern, professional, icon-first design inspired by Swiss editorial design.

### Components and icons
- Use **real SVG icons, logos, or symbols** from reliable sources such as Lucide, Simple Icons, official vendor icon libraries, or other suitable public SVG repositories.
- Never use emoji, Unicode characters, or text-based symbols as substitutes for icons.
- Place each icon above its label, or use a consistent side-by-side arrangement when appropriate.
- **Do not draw boxes, cards, borders, or filled backgrounds around individual icons and labels** unless the chosen diagram convention genuinely requires them.
- Keep labels directly beneath their associated icons, with consistent spacing and alignment.
- Use official brand logos when identifying a specific vendor or technology, and generic icons for conceptual components.
- Never invent a logo or misrepresent a generic icon as an official brand logo.
- If an appropriate real icon cannot be sourced, use a simple native vector shape rather than a textual symbol.

### Layout
- Arrange components in a logical reading order, usually left-to-right or top-to-bottom.
- Group related components using subtle swimlanes, section headings, boundaries, or light background regions where useful.
- Avoid unnecessary containers, decorative graphics, excessive colors, and visual clutter.
- Use consistent icon sizes, typography, alignment, spacing, and connector styles.
- Keep labels concise but sufficiently descriptive.
- Prevent overlapping labels, icons, connectors, and section headings.
- Use orthogonal connectors for complex layouts when appropriate.
- Use arrowheads and line styles consistently to distinguish direction, optional flows, dependencies, asynchronous events, or other relationships when relevant.
- Add a legend only when the visual encoding needs explanation.
- Optimize the canvas for readability and fit-to-page viewing.

### Color and typography
- Use a restrained, accessible palette with neutral backgrounds and a small number of meaningful accent colors.
- Use color to communicate categories or flow types, not merely for decoration.
- Use a consistent, readable sans-serif font.
- Maintain adequate contrast and whitespace.

## 3. Technical Accuracy

Adapt these rules to the selected diagram type.

For system architecture and data-flow diagrams:
- Show component boundaries, external systems, trust boundaries, and important data flows when relevant.
- Distinguish synchronous requests from asynchronous events where useful.
- Include data stores, APIs, queues, external services, and operational components when they materially affect the architecture.
- Show security, authentication, observability, error handling, and reliability mechanisms when relevant to the requested detail level.
- Do not imply that a connection, integration, or capability exists unless supported by the input or explicitly labeled as an assumption.

For process and workflow diagrams:
- Use proper start/end nodes, actions, decision branches, and labeled transitions where appropriate.
- Ensure that branches and paths are logically consistent.

For data models and UML:
- Use appropriate entity, relationship, cardinality, class, sequence, or deployment notation.
- Preserve valid relationships and diagram-specific conventions.

For other diagram types:
- Follow the relevant established notation rather than applying architecture-specific rules indiscriminately.

## 4. SVG and draw.io Compatibility

- Generate a valid, editable `.drawio` XML document that opens in diagrams.net.
- Use supported draw.io XML structures for nodes, edges, labels, and geometry.
- Use actual SVG images for external icons, not emoji or textual placeholders.
- Prefer stable, direct SVG asset URLs. Avoid webpage URLs that merely display an icon preview.
- If practical, embed SVG assets directly in the XML so the diagram remains portable and works offline.
- If using external URLs, ensure they point to actual SVG assets and explain the internet dependency.
- Preserve the ability to move, resize, relabel, reconnect, and edit diagram elements in draw.io.
- Keep icons separate from their labels when this improves editability.
- Use unique cell IDs and valid XML escaping, including `&amp;` for ampersands in XML attributes.
- Do not include unsupported attributes or fabricate asset URLs.

## 5. Quality Assurance

Before returning the result, check:

1. **Semantic correctness:** Does the diagram represent the subject accurately?
2. **Structural correctness:** Are the relationships, paths, dependencies, and directions valid?
3. **Visual quality:** Are components aligned, spaced, readable, and uncluttered?
4. **Icon quality:** Are icons actual SVG graphics rather than emoji or text symbols?
5. **Consistency:** Are labels, arrows, colors, and visual conventions consistent?
6. **XML validity:** Is the XML well-formed and importable into draw.io?
7. **Completeness:** Are important components, branches, and relationships missing?
8. **Portability:** Are external assets reliable, or are their limitations clearly stated?

Correct any detected problems before delivering the output.

## 6. Output Requirements

Return:

1. **The completed diagram** as editable draw.io XML.
2. The complete XML inside a single `xml` code block, unless a downloadable `.drawio` file is explicitly requested or can usefully be provided alongside it.
3. A brief explanation of the diagram's structure and any important assumptions.
4. A short note identifying external SVG dependencies or offline limitations, if applicable.

Do not return pseudocode, partial XML, Mermaid, a static image, or a textual description in place of the requested draw.io XML.

Do not claim that the XML has been validated or that icons have been tested unless those checks were actually performed.

**Priority order:** Technical correctness → appropriate diagram conventions → readability → real icons → visual polish.

Now create the diagram from my input:

[INSERT YOUR SYSTEM, PROCESS, OR CONCEPT HERE]
