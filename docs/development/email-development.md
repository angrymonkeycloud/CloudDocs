
# Email Development Standards

HTML email development must prioritize rendering consistency across legacy and modern email clients.

## Rendering Constraints

- Many email clients use outdated rendering engines.
- Support for modern CSS and JavaScript is limited.
- div-based responsive techniques are not universally reliable.

## Required Structure

- Build email layouts using tables and nested tables.
- Keep markup simple and conservative.
- Inline or email-safe styling should be prioritized.

## Safe Font List

Use broadly supported fonts for fallback-safe rendering:

- Arial
- Verdana
- Helvetica
- Georgia
- Tahoma
- Lucida
- Trebuchet
- Times New Roman

## Quality Checklist

- Test in major inbox clients before release.
- Validate spacing and alignment consistency.
- Validate fallback behavior for unsupported styles.
