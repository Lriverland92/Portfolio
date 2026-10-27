Portfolio Design System

Project Description

This project is a responsive design system for my portfolio. It demonstrates colors, typography, spacing, buttons, cards, forms, and dark and light themes.

Design Decisions

Reset: I used box-sizing: border-box to include padding and borders in element widths. I removed the default body margin to control page spacing.

Tokens: I organized CSS variables into colors, spacing, sizing, rounded corners, shadows, typography, and semantic theme tokens.

Fonts: I used Arial for body text and Georgia for headings. Both are system fonts, with fallback fonts defined in CSS.

Themes: The dark theme is the default. The light theme uses .theme-light to override theme variables without rewriting the component styles.

Accessibility: I used visible keyboard focus indicators, labeled form controls, and tested color contrast.

Testing Record

Test 1: Responsive Design — 320px

Expected Result: The page should fit the screen without horizontal scrolling.

Observed Result: The content fit within the screen, but the original 32px padding reduced the space available for content.

Revision: I changed the padding to clamp(1rem, 3vw, 2rem). Chrome DevTools confirmed that the padding became 16px at 320px.

Test 2: Responsive Design — 768px

Expected Result: The layout should adjust to the available screen width without horizontal scrolling.

Observed Result: The cards displayed in two columns, and the content fit within the screen.

Revision: None.

Test 3: Responsive Design — 1280px

Expected Result: The page should display correctly on a desktop screen.

Observed Result: The content, cards, and form controls displayed correctly.

Revision: None.

Test 4: Browser Zoom — 200%

Expected Result: The page should remain readable without content being cut off.

Observed Result: The text and components remained readable at 200% zoom.

Revision: None.

Test 5: Keyboard Navigation

Expected Result: I should be able to navigate through links, buttons, and form controls using the keyboard, with visible focus indicators.

Observed Result: I used Tab to navigate through the interactive elements and could see the focus indicators.

Revision: None.

Test 6: Color Contrast

Expected Result: Essential text, buttons, links, focus indicators, and form controls should have sufficient contrast against their backgrounds in both themes.

Observed Result: The color combinations I checked using the WebAIM Contrast Checker passed all tests.

Revision: None for the combinations tested.

Test 7: Font Fallback

Expected Result: The browser should display a fallback font if the preferred font is unavailable.

Observed Result: I temporarily changed the preferred font names to unavailable fonts. The browser displayed fallback fonts, and the text remained readable.

Revision: None. I restored the original font names after testing.

Test 8: HTML and CSS Validation

Expected Result: The HTML and CSS should pass validation without errors.

Observed Result: The HTML passed validation using the Nu HTML Checker, and the CSS passed the W3C CSS Validator before the final padding change.

Revision: The CSS still needs to be validated again after the final responsive padding change.

Test 9: Published Website

Expected Result: The published website should load correctly in a private browser window, including its CSS, fonts, links, and form controls.

Observed Result: Not tested yet.

Revision: Pending publication and verification.

Evidence-Based Revision

During responsive testing at 320px, I checked the page spacing using Chrome DevTools. The original 32px padding left less space for content.

I changed the padding to clamp(1rem, 3vw, 2rem) so the spacing could adjust to the screen width.

After making the change, I tested the page again at 320px and confirmed that the padding was reduced to 16px. This gave the content more horizontal space.

Code Defense

Reset Strategy: I used a small CSS reset instead of removing all browser styles. I used box-sizing: border-box to make element widths easier to manage and removed the default body margin so I could control the spacing.

Token Hierarchy: I defined my main colors, spacing, fonts, sizes, borders, and shadows using CSS variables in :root. I also created semantic theme variables such as --theme-background, --theme-text, and --theme-button. These variables let me change the appearance of components without changing every individual CSS rule.

Scoped Theme Override: I used .theme-light to change the semantic theme variables for the alternate light theme. The components use the same CSS rules in both themes.

Evidence-Based Revision: I changed the page padding after testing the design at 320px. I verified the change using the Chrome DevTools.

AI Disclosure
ChatGPT was used to suggest token names, write generic placeholder text, and troubleshoot responsive spacing.  I selected the color palette, reviewed the code, and tested the page using the webAIM and NuHTML validators. 

Repository URL

https://github.com/Lriverland92/Portfolio

Website URL

https://lriverland92.github.io/Portfolio/