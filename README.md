🖋️ Strike Through Activity

An interactive checklist component designed for content verification and progressive disclosure of information. This activity allows users to visually "cross off" items as they process them, enhancing engagement with long lists.

🚀 Live Demo

Explore the Strike Through Activity Component Here

✨ Project Overview

The Strike Through Activity provides a tactile sense of progress for educational or procedural content. It transforms a standard list into an interactive experience where each item responds to user input with multiple visual state changes.

Key Features

Visual Progress Feedback: Clicking an item triggers a coordinated UI response:

The text receives a line-through decoration.

The item opacity drops to 0.7 to indicate a "completed" status.

The circular checkbox fills with a brand-consistent Teal color.

Micro-interactions:

Hover Animation: Items scale slightly and shift to the right (translateX(5px)), signaling interactivity.

State Toggling: Users can easily undo a selection by clicking the item again.

Accessible Instruction: Features clear instructional text (instruction-text) positioned at the top to guide the user's interaction.

Structured Content Area: Includes an introductory text area and a footer note section for comprehensive context around the checklist.

🛠️ Technical Implementation

State Management: Uses a simple yet effective toggleItem(element) JavaScript function that utilizes classList.toggle('completed'). This approach keeps the logic decoupled from the content.

CSS Architecture:

Checkmark SVG: Uses an inline SVG for the check icon, ensuring it scales perfectly and remains crisp on high-resolution displays.

Transitions: All state changes (hover, background color, text decoration) use a cubic-bezier timing function for a smooth, high-quality feel.

Flexbox Alignment: The checklist items use display: flex with align-items: center to ensure the circular checkbox and text remain perfectly aligned regardless of text length.

📂 Design Tokens

Midnight Blue (#1f2a52): Primary color for the header bar and main text.

Teal (#00bec7): Accent color for instructions, checkboxes, and active checkmarks.

Light Aqua (#d2f0f0): Used for item borders and the footer divider.

Slate Grey (#abb5bf): The "completed" state color for text and borders, providing a visual "dimming" effect.

📖 Usage Instructions

To add new items to the checklist, follow this HTML structure inside the ul.checklist container:

<li class="checklist-item" onclick="toggleItem(this)">
    <div class="check-circle">
        <svg class="check-icon w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path>
        </svg>
    </div>
    <span class="item-text">Your item content goes here.</span>
</li>


📄 License

MIT License - Developed as part of the accounts-eles UI component library.
