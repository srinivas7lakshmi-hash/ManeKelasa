# Product Requirements Document (PRD): Mane-Kelsa

## 1. Project Overview
- **Project Name:** Mane-Kelsa
- **Status:** v2.0.0 (Production Ready)
- **Tagline:** Connecting local hands to local homes.

## 2. Problem Statement
Domestic workers in small towns lack a platform to showcase their availability, while residents lack a central directory to find reliable help. This local fragmentation leads to inefficient labor utilization and inconsistent service for households.

## 3. Proposed Solution
A lightweight, multilingual web application that acts as a localized directory. It provides workers with a "digital identity card" showing their skills, rates, and availability, while allowing users to find and call help with a single tap.

## 4. Key Features
### 4.1. Localization (L10n)
- Support for **Kannada, English, and Hindi**.
- One-tap language switching without page reloads.

### 4.2. Worker Management
- **Availability State:** Real-time visibility of whether a worker is taking calls or on a break.
- **Skill Mapping:** Categorized icons for Cleaning, Gardening, and Washing.
- **Rating System:** Community-driven feedback via a "Thumbs Up" mechanism.

### 4.3. Search and Discovery
- Search by name, skill, or area (e.g., "Vidyagiri", "Gandhinagar").
- Availability-based filtering to ensure high response rates.

### 4.4. User Experience
- **Mobile-First Design:** Optimized for touch targets (44px+) and bottom navigation.
- **Dark Mode:** Reduces eye strain and saves battery on mobile OLED screens.
- **Frictionless Calling:** "Call Now" button opens the phone's native dialer directly.

## 5. Technology Stack
- **React 18:** Modern UI framework.
- **TypeScript:** Ensuring robust development and error prevention.
- **Tailwind CSS:** Efficient, responsive styling with a custom "Nature-Tech" emerald theme.
- **Framer Motion:** High-quality micro-interactions for a premium feel.
- **Lucide Icons:** Clean, consistent iconography.

## 6. Success Metrics
- **Response Time:** Time taken from search to initiating a call.
- **Accessibility:** Ease of use for non-English speakers (measured by language switch frequency).
- **Retention:** User profile completion rate.

## 7. Development Roadmap
- **Phase 1 (Complete):** Core UI, Multilingual support, LocalStorage persistence.
- **Phase 2 (Current):** Search optimization and Profile management.
- **Phase 3 (Future):** Firebase Backend for real-time multi-user data sync and cloud authentication.
