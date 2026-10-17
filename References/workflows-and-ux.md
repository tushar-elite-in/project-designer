# Workflows and user experience

Plan around real tasks, not a feature list alone.

## Workflow design

For each actor or role, document:
- Goal and starting state.
- Preconditions, permissions, and data available.
- Main steps and system responses.
- Success state and confirmation.
- Important error, cancellation, empty, timeout, and recovery paths.
- Notifications or human handoffs, if required.

Use a role/action matrix where access differs. Distinguish authentication (who is signed in) from authorization (what they may do). Map key journeys to the features and acceptance checks.

## Interface scope

Identify target form factors, input methods, language/locale, connectivity, assistive technology needs, and design references. Treat supplied wireframes as mandatory or illustrative according to the source. Define screen/page inventory and navigation only to the level needed to communicate scope.

## Accessibility and platform fit

For web content, consider semantic structure, keyboard access, focus visibility, contrast, labels, errors, target size, captions/alternatives, responsive zoom/reflow, and accessible interaction states. Use the current WCAG recommendation as a reference when applicable; the target level must come from the user, contract, or law, not be invented.

For native apps, consult the official platform human-interface and accessibility guidance for the target OS and device. Do not force web interaction patterns onto native products or assume one platform's conventions apply to another.

Accessibility claims require verification; a plan or automated scan alone is not proof of conformance.