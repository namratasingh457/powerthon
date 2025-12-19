# Design Guidelines: Price-Locked Subscription E-Commerce Platform

## Design Approach
**Reference-Based**: Drawing from modern e-commerce leaders (Shopify, Stripe Billing) and SaaS subscription platforms (Notion pricing pages). Focus on trust-building, clear value communication, and seamless conversion flows.

## Core Design Principles
1. **Price Transparency**: Make savings and locked prices immediately visible
2. **Conversion-Focused**: Clear CTAs and trust signals throughout
3. **Premium Feel**: Polished aesthetics that justify subscription value
4. **Data Clarity**: Easy comparison between market vs locked prices

---

## Typography System

**Font Families** (Google Fonts):
- **Display/Headings**: Inter (700, 800 weights)
- **Body/UI**: Inter (400, 500, 600 weights)

**Scale**:
- Hero Headlines: text-5xl to text-6xl, font-bold
- Section Headers: text-3xl to text-4xl, font-bold
- Card Titles: text-xl, font-semibold
- Body Text: text-base, font-normal
- Captions/Meta: text-sm, font-medium
- Price Tags: text-2xl to text-3xl, font-bold
- Discount/Savings Labels: text-sm, font-semibold, uppercase tracking-wide

---

## Layout System

**Spacing Units**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24
- Component padding: p-4 to p-8
- Section spacing: py-16 to py-24
- Card gaps: gap-6 to gap-8
- Grid spacing: grid with gap-6

**Container Strategy**:
- Full-width: w-full with max-w-7xl mx-auto px-4
- Content sections: max-w-6xl
- Text content: max-w-4xl

---

## Component Library

### Navigation
**Desktop Header**: Fixed top navigation with logo left, main nav center, account/cart right. Includes "Subscribe" CTA button (prominent treatment). Height: h-20, backdrop-blur-lg with subtle shadow on scroll.

### Hero Section
**Full-width immersive hero** (h-[600px]) with high-quality lifestyle product image showing subscription value. Overlay with blurred backdrop for text/CTAs. Includes:
- Bold headline emphasizing price-locking benefit
- Subheadline explaining the value proposition
- Primary CTA "Start Free Trial" + Secondary CTA "View Plans"
- Trust indicators (user count, savings stats)

### Subscription Tier Cards
**Three-column grid** (grid-cols-1 md:grid-cols-3 gap-8) with distinct tier cards:
- Card structure: Rounded corners (rounded-2xl), elevated shadow
- Tier badge at top (ribbon or pill shape)
- Large price display with period indicator
- Feature list with checkmark icons (Heroicons)
- Prominent CTA button per tier
- "Most Popular" tier gets accent treatment (border, subtle background glow)

### Product Grid
**Multi-column responsive grid** (grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6):
- Product cards with image (aspect-square), title, current price
- **Price comparison badge**: Shows locked price vs market price with savings percentage (positioned top-right of card)
- For non-subscribers: "Subscribe to lock this price" message
- Hover state: Subtle lift effect (scale-105 transition)

### Price Lock Dashboard
**Split-view layout** for subscribed users:
- Left column (60%): Product grid with locked prices highlighted
- Right sidebar (40%): Savings summary card, subscription details, locked price list
- Visual indicators: Green checkmarks for locked prices, upward arrows showing market price increases

### Shopping Cart/Checkout
**Single column on mobile, two-column on desktop**:
- Left: Cart items with locked vs current price display
- Right: Order summary with total savings highlighted
- Sticky summary on scroll
- Progress indicator for checkout steps

### Pricing Comparison Table
**Feature comparison grid** for subscription tiers:
- Sticky header row with tier names
- Left column: Feature categories
- Checkmarks/crosses for feature availability (Heroicons)
- Highlight cells for premium features

### Footer
**Four-column layout** (grid-cols-2 md:grid-cols-4):
- Quick links, Product categories, Support, Newsletter signup
- Social media icons (Font Awesome)
- Trust badges (secure payment, money-back guarantee)
- Compact height: py-12

---

## Icons
**Font Awesome** (via CDN) for:
- Shopping cart, user account, lock (price-lock), check circles, arrows (trends), credit card, shield (trust badges)

---

## Images

**Hero Section**: Full-width lifestyle image showing products in aspirational context (e.g., organized home pantry, tech workspace). Resolution: 1920x600px minimum. Apply dark overlay (bg-black/40) for text readability.

**Product Images**: Square aspect ratio (400x400px), clean white/neutral backgrounds, professional product photography style.

**Subscription Benefits Section**: 3 supporting images (600x400px) showing different customer scenarios benefiting from price locks.

**Trust Section**: Customer photos (circular crop, 80x80px) for testimonials.

---

## Interaction Patterns

**Micro-interactions** (minimal, purposeful):
- Price comparison tooltip on hover
- Savings counter animation on scroll into view
- Smooth transitions for cart updates (300ms ease)
- Tier card selection state with subtle border glow

**No complex animations** - focus on instant feedback and clarity.

---

## Accessibility

- Minimum touch targets: 44x44px for all interactive elements
- Color contrast ratio: 4.5:1 for all text
- Form inputs: Clear labels, visible focus states (ring-2)
- Price indicators: Include text descriptions, not just color coding
- Keyboard navigation: Full tab order for all interactive elements

---

## Key UX Patterns

**Progressive Disclosure**: Show basic pricing first, expand to detailed comparisons on demand

**Social Proof**: Display subscriber count, total savings across platform, recent sign-ups

**Urgency Indicators**: "Price increasing soon" labels on products where market prices will change

**Value Reinforcement**: Throughout checkout, repeatedly show savings from locked prices

**Trust Signals**: Secure payment badges, money-back guarantee, customer testimonials prominently placed