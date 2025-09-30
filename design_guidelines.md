# Design Guidelines: Personal Blog Navigation Hub

## Design Approach
**Selected Approach:** Custom Landing Page with Image-First Design

This is a single-purpose navigation hub that prioritizes visual impact and clarity. The design will create an immersive experience around the background image while ensuring buttons remain prominent and accessible.

## Core Design Elements

### A. Color Palette

**Dark Mode (Primary):**
- Background Overlay: 0 0% 0% / 0.4 (semi-transparent black overlay over image)
- Text Primary: 0 0% 100% (pure white)
- Text Secondary: 0 0% 90% (off-white)
- Button Background: 0 0% 100% / 0.15 (frosted glass effect)
- Button Border: 0 0% 100% / 0.3
- Button Hover: 0 0% 100% / 0.25

**Light Mode Alternative:**
- Background Overlay: 0 0% 100% / 0.3
- Text Primary: 0 0% 10%
- Button Background: 0 0% 0% / 0.1
- Button Border: 0 0% 0% / 0.2

### B. Typography

**Font Families:**
- Primary: 'Inter' or 'Poppins' from Google Fonts for clean, modern readability
- Weight: 600-700 for headings, 400-500 for body text

**Text Hierarchy:**
- Welcome Heading: text-5xl md:text-7xl font-bold (large, impactful)
- Subtitle (if added): text-xl md:text-2xl font-medium
- Button Text: text-lg font-semibold

### C. Layout System

**Spacing Primitives:** Use Tailwind units of 4, 6, 8, 12, and 16
- Container padding: p-8 md:p-16
- Button spacing: gap-6
- Vertical rhythm: space-y-8

**Page Structure:**
- Full viewport height (min-h-screen)
- Centered content using flexbox
- Maximum content width: max-w-4xl for button container

### D. Component Specifications

**Background Image Treatment:**
- Full-screen background (bg-cover bg-center bg-fixed)
- Image URL: https://ibb.co.com/PZNZDKJp
- Dark gradient overlay (gradient-to-b from-black/40 via-black/30 to-black/50)
- Ensures text readability across all image areas

**Welcome Text:**
- Centered alignment
- White color with subtle text shadow for depth (drop-shadow-lg)
- Animated entrance (fade-in with slight slide-up)
- Positioned above buttons with mb-12 spacing

**Navigation Buttons:**
- Three buttons in vertical stack on mobile, horizontal row on desktop (flex-col md:flex-row)
- Glassmorphism style: backdrop-blur-md with semi-transparent backgrounds
- Large touch targets: px-12 py-6 (generous padding)
- Rounded corners: rounded-xl
- White borders with opacity (border-2 border-white/30)
- Each button width: w-full md:w-auto md:min-w-[200px]
- Hover state: Increase background opacity and scale slightly (transform scale-105)

**Button Labels & Links:**
1. "Sajak" → sajakpann.blogspot.com
2. "Quotes" → quotespann.blogspot.com  
3. "Pendapat" → pendapatpann.blogspot.com

### E. Responsive Behavior

**Mobile (< 768px):**
- Vertical button stack with gap-4
- Smaller welcome text (text-4xl)
- Reduced padding (p-6)

**Desktop (≥ 768px):**
- Horizontal button layout with gap-6
- Larger welcome text (text-7xl)
- Generous padding (p-16)

### F. Interactive States

**Buttons:**
- Default: Semi-transparent with blur, crisp borders
- Hover: Increased opacity, subtle scale, smooth transition (300ms)
- Active: Slight scale reduction
- Focus: Prominent outline for keyboard navigation

## Images

**Hero Background Image:**
- Position: Full-page background covering entire viewport
- Treatment: Apply dark gradient overlay for text contrast
- Behavior: Fixed attachment for parallax effect on scroll (if page extends)
- Fallback: Dark gradient background (in case image fails to load)

## Additional Enhancements

**Accessibility:**
- High contrast text on all backgrounds
- Focus indicators for keyboard navigation
- Sufficient button sizing for touch targets (minimum 48px height)
- Alt text for background image context

**Performance:**
- Optimize background image delivery
- Lazy load if implementing any additional content below fold
- Use CSS backdrop-filter for performant glass effects

**Polish:**
- Subtle entrance animations (fade-in, slide-up) on page load
- Smooth transitions on all interactive elements (300ms ease)
- Ensure buttons remain readable regardless of background image complexity through overlay and blur techniques

This design creates a visually striking, memorable first impression while maintaining absolute clarity of purpose—directing users to the three blog destinations with style and confidence.