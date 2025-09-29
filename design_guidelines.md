# Design Guidelines: Diablo Recon Web Interface

## Design Approach: Function-First Design System
**Justification**: As a professional OSINT reconnaissance tool, this application prioritizes efficiency, data clarity, and investigative workflow over visual flair. The design should support rapid username searches and clear result presentation.

**Design System**: Material Design with security/terminal aesthetic adaptations
**Key Principles**: 
- Information hierarchy for rapid scanning
- Professional, serious tone appropriate for security research
- Dark theme optimized for extended use
- Minimal cognitive load during investigations

## Core Design Elements

### A. Color Palette
**Dark Mode Primary** (matching terminal aesthetic):
- Background: 0 0% 8% (dark charcoal)
- Surface: 0 0% 12% (slightly lighter panels)
- Primary brand: 0 85% 55% (red accent, matching tool's terminal colors)
- Text primary: 0 0% 95% (near white)
- Text secondary: 0 0% 70% (medium gray)
- Success: 120 60% 50% (green for found profiles)
- Warning: 45 100% 60% (amber for partial results)
- Error: 0 85% 55% (red for errors)

**Light Mode Alternative**:
- Background: 0 0% 98%
- Surface: 0 0% 100%
- Primary: 0 75% 45% (darker red for accessibility)

### B. Typography
**Font Families**: 
- Primary: Inter (clean, readable for data display)
- Monospace: JetBrains Mono (for usernames, URLs, technical data)

**Type Scale**:
- Headers: 24px, 20px, 18px (semibold)
- Body: 16px (regular), 14px (medium for secondary info)
- Captions: 12px (for metadata, timestamps)

### C. Layout System
**Spacing Units**: Tailwind scale focused on 4, 6, 8, 12, 16, 24px
- Consistent 4-unit grid system
- Component spacing: p-4, p-6 for cards
- Section spacing: mb-8, mt-12 for major sections
- Tight spacing: gap-2, gap-4 for related elements

### D. Component Library

**Core Components**:
- **Search Form**: Clean input with search button, real-time validation
- **Progress Indicator**: Linear progress bar with site counter and status
- **Results Table**: Dense data table with site categories, status indicators, and clickable profile links
- **Filter Sidebar**: Collapsible category filters (Social, Gaming, Forums, etc.)
- **Export Panel**: Action buttons for TXT/PDF export with download status
- **Statistics Dashboard**: Key metrics cards (found profiles, completion rate, search time)

**Navigation**: 
- Minimal top navigation with search history access
- Sidebar for filtering and categories
- Breadcrumb-style search state indicators

**Data Display**:
- Compact table rows with status badges
- Color-coded profile availability (green=found, red=not found, yellow=checking)
- Expandable details for metadata when available

**Forms**:
- Single prominent search input
- Advanced options collapsed by default
- Clear field labels and validation states

**Overlays**:
- Modal for search settings and export options
- Toast notifications for export completion
- Loading states for long-running searches

### E. Animations
**Minimal Animation Strategy**:
- Smooth progress bar updates during search
- Subtle fade-in for search results
- Basic hover states on interactive elements
- No decorative animations to maintain professional focus

## Images
**No Hero Image**: This is a utility application focused on data processing, not marketing
**Iconography**: Use Material Icons or Heroicons for:
- Search, filter, export actions
- Platform category icons (social media, gaming, etc.)
- Status indicators (checkmarks, X marks, loading spinners)
- Small avatar placeholders for found profiles

The interface should feel like a professional security research tool - clean, efficient, and information-dense without visual distractions.