**SPECIFICATIONS: Interactive Feng Shui & Qimen Dunjia Foundations App**

**Purpose:** To build an interactive web app helping users understand the basics of Feng Shui based on the 后天八卦 (Houtian Ba Gua) / 九宫格 (Jiu Gong Ge) model, the fundamentals of 五行 (Wu Xing), and how 奇门遁甲 (Qimen Dunjia) Eight Gates (八门) can be conceptually integrated with the 二十四山 (24 Mountains). This app serves as a foundational learning tool for the "水到奇成" course.

**General Requirements:**

1.  **Technology Stack:**
    *   Single, self-contained HTML document using only inline HTML5, CSS3, and vanilla JavaScript.
    *   No external libraries are allowed.
    *   Code within the single file should be well-structured with clear commenting (e.g., CSS rules grouped by component, JS functions grouped by feature) for maintainability.

2.  **Visual Design & UX:**
    *   The visual style must be clean, minimalist, and highly readable.
    *   Effective visual hierarchy (e.g., font sizes, weights, spacing) must be used to guide the user's attention, especially in information-dense areas like the info panel.
    *   The User Interface (UI) must be intuitive, especially the controls for overlays and language switching.
    *   All interactive elements (buttons, clickable grid cells/segments) must have clear hover, active, and focus states for immediate visual feedback.
    *   Subtle, non-jarring CSS transitions (e.g., fade-in/out, slide) should be considered for actions like opening/closing the info panel or switching overlays to enhance smoothness.
    *   The app must be fully responsive, ensuring optimal functionality and readability on both desktop and mobile devices.
        *   Prioritize clarity on smaller screens.
        *   Ensure touch targets (buttons, grid cells, segments) are adequately sized for mobile (e.g., minimum 44x44px effective area) to prevent mis-taps.

3.  **Localization:**
    *   The app must support **Chinese (Simplified - default)** and **English**.
    *   A clear and easily accessible mechanism (e.g., a dropdown or toggle buttons in a fixed/sticky header or footer) must be provided for users to switch languages. This switcher must remain visible even when the info panel is open or content is scrolled.
    *   All display text, labels, and informational content must be translated.
    *   The selected language preference should be persisted (e.g., using `localStorage`) so users do not have to re-select it on subsequent visits or page refreshes.

4.  **App Title:**
    *   A clear title "后天八卦 (Houtian Ba Gua) / 九宫格 (Jiu Gong Ge) Foundations" (with its English equivalent "Later Heaven Ba Gua / Nine Palaces Grid Foundations") should be displayed prominently above the main grid, respecting the selected language.
    *   Consider including the course name "水到奇成 Course" subtly in the footer or an "About" section for branding reinforcement.

**Detailed Specifications:**

1.  **Central Element: The Ba Gua Grid**
    *   The app will present a 3x3 grid, serving as the central interactive element.
    *   The arrangement of the 8 outer cells must follow the standard Houtian Ba Gua sequence:
        *   Top Row (L-R): 巽 Xun (SE), 離 Li (S), 坤 Kun (SW)
        *   Middle Row (L-R): 震 Zhen (E), 中宫 Zhong Gong, 兌 Dui (W)
        *   Bottom Row (L-R): 艮 Gen (NE), 坎 Kan (N), 乾 Qian (NW)
    *   The center cell of the grid will be visually distinct (e.g., a slightly different, neutral background) and labeled "中宫 (Zhong Gong - Central Palace)" (with English translation). It will **not** be clickable for detailed attribute information in any mode or overlay configuration.

2.  **Ba Gua Mode (Default View):**
    *   Each of the 8 outer cells in the grid should be clearly and concisely labeled, with a consistent display order (e.g., 1. Trigram Symbol, 2. Trigram Name, 3. Direction):
        *   Its corresponding **Trigram Symbol** (e.g., ☰, ☵).
        *   Its **Trigram Name** (e.g., 乾 Qian).
        *   Its associated **Direction** (e.g., 西北 Northwest). *(Translations for names and directions required).*
    *   **Visual Cue:** A subtle, non-intrusive background color tint representing the cell's primary Element can be applied to each of the 8 outer cells (e.g., light blue for Water, light green for Wood). Ensure sufficient color contrast between the background tint and text labels for readability (WCAG AA compliance).

3.  **Interactivity in Ba Gua Mode:**
    *   Users must be able to click on each of the 8 outer cells.
    *   Upon clicking a cell, a designated information panel (e.g., a well-styled modal popup or a dynamic sidebar section) should appear. This panel must be designed to handle varying amounts of information clearly. Content should be scrollable if necessary, especially on mobile.
    *   The info panel must be dismissible via clear methods (e.g., an "X" button, clicking outside the panel area, pressing the Escape key).
    *   The panel will display the following attributes for the selected cell (all text translatable):
        *   **Trigram Symbol** and **Trigram Name**.
        *   **Direction:** e.g., "北 North (conceptually encompassing the 壬 Ren, 子 Zi, 癸 Gui mountains, which are used for precise orientation in advanced Feng Shui)."
        *   **Element** associated with that trigram (e.g., 水 Water).
        *   **General Qualities:** A short sentence describing aspects of life that trigram represents (e.g., "乾 (Qian) represents Heaven, strength, and leadership.").
        *   **Enhancement Potential:** A concise description of what that Element in that position can enhance (e.g., "The Water element in the North can enhance career flow and wisdom.").
        *   **五行 (Wu Xing) Interactions (clearly sectioned, including Pinyin):**
            *   "Generates (生 shēng): [Element it generates] (e.g., Water generates Wood / 水生木 Shuǐ shēng Mù)"
            *   "Controls (克 kè): [Element it controls] (e.g., Water controls Fire / 水克火 Shuǐ kè Huǒ)"
            *   "Is Generated By (被生 bèi shēng): [Element that generates it] (e.g., Water is generated by Metal / 金生水 Jīn shēng Shuǐ)"
            *   "Is Controlled By (被克 bèi kè): [Element that controls it] (e.g., Water is controlled by Earth / 土克水 Tǔ kè Shuǐ)"

4.  **Qimen Dunjia Overlay Mode:**
    *   **Activation Button:** A clearly visible button labeled "Show Qimen Gates (八门)" (with English translation, changing to "Hide Qimen Gates" when active) must be present. This button should have distinct visual states for "on" and "off" (e.g., color change, icon change).
    *   When toggled on:
        *   New labels for the **Eight Gates (八门)** appear prominently within each of the 8 outer cells, *in addition* to existing Ba Gua labels.
        *   Each cell is labeled with the Gate that **originates** from its Ba Gua location (fixed "home palace" mapping):
            *   休门 (Xiu Men) in 坎 (Kan) Palace
            *   生门 (Sheng Men) in 艮 (Gen) Palace
            *   伤门 (Shang Men) in 震 (Zhen) Palace
            *   杜门 (Du Men) in 巽 (Xun) Palace
            *   景门 (Jing Men) in 离 (Li) Palace
            *   死门 (Si Men) in 坤 (Kun) Palace
            *   惊门 (Jing Men - different Jing) in 兑 (Dui) Palace
            *   开门 (Kai Men) in 乾 (Qian) Palace
        *   **Label Clarity Strategy:** To ensure labels do not excessively overlap:
            *   Consider a slightly smaller font for Gate names when the overlay is active.
            *   Position Gate names consistently (e.g., below the Ba Gua name).
            *   If necessary for extreme space constraints on the grid, Gate names could be abbreviated (e.g., "开" for "开门"), with full names always available in the info panel.
        *   The Central Palace ("中宫") cell, when this overlay is active, displays a simple, generic star symbol (e.g., ★ or ☆) without further interactive detail.

5.  **Interactivity in Qimen Dunjia Overlay Mode:**
    *   When the "Overlay Qimen Gates" mode is active, clicking on an outer cell updates the information panel to display, with clear visual separation (e.g., headings, horizontal rules) between sections:
        *   **All information from Ba Gua Mode (Spec 3)** for context.
        *   **AND additional Qimen Gate Information (clearly sectioned):**
            *   **Gate Name** (e.g., "开门 (Kai Men) - Open Gate").
            *   **Original Palace & Derived Element:** "Originates from: [Original Ba Gua Palace Name, e.g., 乾 (Qian) Palace]. Derived Element: [Gate's intrinsic Element, e.g., 金 (Metal)]."
            *   **General Gate Properties:** (e.g., "The Open Gate (开门) is generally auspicious for new beginnings...").
            *   **Conceptual Interaction Explanation (Setting Stage for Course):**
                *   "Fundamental State: In this view, the [Gate Name] is in its home palace ([Palace Name]), where its element ([Gate's Element]) aligns with the palace's element ([Palace's Element])." (Ensure dynamic placeholders are correctly populated).
                *   "Course Insight: The '水到奇成' course teaches how this Gate's energy dynamically changes when it moves to *other* palaces in a time-specific Qimen chart. Identifying unfavorable interactions or conditions ('四害 - Si Hai' / 'problem indicators') in those dynamic contexts is key and will be covered in the course."

6.  **Static Informational Sections (Accessible, e.g., via clearly labeled buttons/links in a header/footer or as collapsible/expandable sections below the main content. Content must be translatable and well-formatted for readability. Collapsible sections must be keyboard accessible and their state clear):**
    *   **A. "How to Use This App":** A brief, potentially dismissible, initial guide on click interactions, overlay toggles, and language switching.
    *   **B. "About 五行 (Wu Xing - The Five Elements)":**
        *   Concise explanation. Visual diagrams (SVG preferred for scalability, with appropriate `aria-label` or `<title>` elements for accessibility) for Generating (相生) and Controlling (相克) cycles with brief descriptions.
    *   **C. "About Directions, 罗盘 (Luopan), & 二十四山 (24 Mountains)":**
        *   Clear explanations of the 8 Ba Gua directions, subdivision into 24 Mountains (each ~15 degrees), the role of the Luopan, and the importance of precise Mountain identification.
        *   Consider including a simple static visual (SVG preferred) showing how a Ba Gua direction is subdivided into its three mountains.
    *   **D. "About this App & Next Steps for '水到奇成' Course":**
        *   Briefly explains the app's purpose. Mentions the course covers dynamic Qimen charts, "四害" identification, and practical application with 24 Mountains.
    *   **E. "Glossary of Terms":** A small section defining key Pinyin/Chinese terms used in the app (e.g., Ba Gua, Wu Xing, specific Gate/Palace names) to assist beginners. Key terms in other sections could link here.

7.  **Feng Shui 二十四山 (24 Mountains) Overlay Mode:**
    *   **7.1. Activation Button:** A clearly visible, separate button labeled "Show 24 Mountains (二十四山)" (with English translation, changing to "Hide 24 Mountains" when active), with distinct visual states for "on" and "off". This overlay can be active independently or in conjunction with the Qimen Gates overlay.
    *   **7.1.1. Overlay Indicator:** The UI must clearly indicate which overlays are active (e.g., persistent visual cues on toggle buttons, a small status area).
    *   **7.2. Visual Representation on the Grid (24 Mountains Overlay Active):**
        *   Each of the 8 outer Ba Gua cells is visually subdivided into three distinct, equal segments (e.g., using subtle internal borders).
        *   Each of these 24 segments is clearly labeled with its **specific Mountain Name** (e.g., 壬 Ren, 子 Zi, 癸 Gui).
            *   **Segment Ordering:** Follow standard Luopan convention for segment order within a palace (e.g., for Kan/North, viewed facing the grid: 壬 Ren (N3) on left, 子 Zi (N2) in middle, 癸 Gui (N1) on right).
            *   **Legibility Strategy:** Use single Chinese characters for Mountain names on the grid (壬, 子, 癸). Full names and Pinyin will be in the info panel. Consider adjusting Ba Gua Trigram/Name size or position if needed. On hover over a Ba Gua cell (when 24 Mountains overlay is active), its three mountain segments could be visually highlighted.
        *   Existing Ba Gua labels remain visible, styled for clarity alongside Mountain segments.
        *   Central Palace is not subdivided.
    *   **7.3. Interactivity with 24 Mountains Overlay Active (Clicking a Mountain Segment):**
        *   The information panel, leading with Mountain-specific info, displays the following for the **selected Mountain** (all text translatable, clearly sectioned):
            *   **A. Mountain Name:** (e.g., "子 (Zi) Mountain").
            *   **B. Parent Ba Gua Palace:** "Belongs to: 坎 (Kan) Palace - 北 (North) Direction."
            *   **C. Approximate Degree Range:** (e.g., "Approx. Degrees: 352.5° - 7.5°"). *Degree data must be accurate based on standard Luopan conventions (internally document source/convention).*
            *   **D. Inherited Element:** "Primary Element: 水 (Water) (from 坎 Kan Palace). Specific Mountain elemental nuances will be explored in the '水到奇成' course."
            *   **E. Brief Feng Shui Implication:** (e.g., "子 (Zi) Mountain: Peak Water energy, direct North. Key for precise house orientation.").
            *   **F. Relevance to "水到奇成" Course:** "Course Essential: Accurately identifying the Facing/Sitting Mountain (e.g., Zi Mountain) with a Luopan (罗盘) is a critical first step in '水到奇成' for overlaying and interpreting the Qimen Dunjia chart."
    *   **7.4. Combined Overlay Interactivity (24 Mountains + Qimen Dunjia Gates Active - Clicking a Mountain Segment):**
        *   The information panel presents a comprehensive, well-organized view, potentially using collapsible sub-sections for Ba Gua/Qimen info to manage density, especially on mobile. The Mountain info (7.3 A-F) should be visible by default.
        *   **Information Hierarchy:**
            1.  **All Mountain information (Spec 7.3 A-F).**
            2.  **Parent Ba Gua Palace Information (briefly, for context).**
            3.  **PLUS, clearly sectioned Qimen Gate information for the parent Ba Gua Palace:**
                *   "Qimen Gate in this Sector: [Gate Name, e.g., 休门 (Xiu Men)] (occupying the [Parent Ba Gua Palace Name, e.g., 坎 (Kan) Palace] in this foundational view)."
                *   The Gate's properties and conceptual interaction (Spec 5, adapted for this context).

**Final Development Considerations:**

*   **Data Management:**
    *   All translatable text, Ba Gua attributes, Gate details, Mountain details, degree ranges, etc., must be stored in well-structured JavaScript objects (e.g., a nested JSON-like structure within the JS code). This facilitates localization (switching between `content.zh.element` and `content.en.element`) and simplifies content updates and maintenance.
    *   Example structure:
        ```javascript
        const appData = {
          settings: { defaultLang: 'zh', currentLang: 'zh' },
          content: {
            zh: { appTitle: "后天八卦...", palaces: { kan: { name: "坎", trigram: "☵", ... } }, /* ... */ },
            en: { appTitle: "Later Heaven Ba Gua...", palaces: { kan: { name: "Kan", trigram: "☵", ... } }, /* ... */ }
          }
        };
        ```
    *   Ensure all translated text grounded with Google Search.    
*   **Initial State & Reset:**
    *   The app should load in a defined initial state: Ba Gua mode active, Chinese (Simplified) language selected, no cell selected, info panel hidden.
    *   Clicking an already selected cell/segment or clicking on a non-interactive area of the grid (if feasible) could deselect it and hide the info panel, acting as a "clear selection" mechanism.
*   **Performance:** Ensure smooth interactions and quick loading times, given all code is inline. Optimize asset handling if SVGs become complex.
*   **Accessibility (A11y):**
    *   **Keyboard Navigation:** All interactive elements (grid cells/segments, buttons, language switcher, info panel close button, collapsible section toggles) must be focusable and operable via keyboard (e.g., using Tab for navigation, Enter/Space for activation).
    *   **ARIA Attributes:** Use ARIA attributes appropriately: `aria-expanded` for collapsible sections, `aria-label` for icon-only buttons or ambiguous links, `aria-live="polite"` for the info panel content updates to inform screen readers of changes, `role="button"` for non-native button elements, etc.
    *   **Semantic HTML:** Use semantic HTML elements where appropriate (e.g., `<nav>`, `<button>`, `<main>`, `<aside>`).
    *   **Color Contrast:** Maintain sufficient color contrast for all text and UI elements as per WCAG AA guidelines.
    *   **Trigram Symbols:** If Trigram symbols (☰, ☵, etc.) are Unicode text characters, test how they are announced by screen readers. If they are SVGs or images, they must have appropriate alt text or `aria-label`.
*   **Code Clarity:** Inline code should still be well-structured, commented, and organized (e.g., functions for rendering UI, handling interactions, managing state, and localization) for maintainability.
*   **Error Handling (Conceptual):** While complex error handling isn't expected, ensure the app is robust and does not break from typical user interactions. Defensive coding for data lookups (e.g., from the content object) is advisable.
*   **Testing:**
    *   Thoroughly test across common modern browsers (Chrome, Firefox, Safari, Edge).
    *   Test on a range of physical device screen sizes or using browser developer tools to emulate mobile, tablet, and desktop views.
    *   Test localization switching thoroughly, ensuring all text elements update correctly.
    *   Perform basic accessibility checks (e.g., keyboard navigation, screen reader output for key elements).