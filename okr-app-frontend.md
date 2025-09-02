# Frontend Design Document for Table Rock OKR Management Platform

## Table of Contents
- [Pages/Screens List](#pages/screens-list)
- [Wireframes or Layout Descriptions](#wireframes-or-layout-descriptions)
- [UI Components](#ui-components)
- [Navigation Structure](#navigation-structure)
- [Color Scheme & Fonts](#color-scheme--fonts)
- [User Flow](#user-flow)
- [Responsiveness](#responsiveness)
- [State Management](#state-management)

## Pages/Screens List
1. **Home**
2. **Dashboard**
3. **Profile**
4. **Login/Register**
5. **OKR Management**
6. **Team Management**
7. **Session Management**
8. **Reports & Analytics**
9. **Admin Settings**
10. **Notifications**
11. **Help/Support**

## Wireframes or Layout Descriptions

### Home
- **Header**: Branding, Login/Register links.
- **Hero Section**: Welcome message, brief description of the platform.
- **Features Overview**: Key platform features with icons and brief descriptions.
- **Footer**: Contact information, legal links.

### Dashboard
- **Header**: User avatar, notifications icon, settings menu.
- **Sidebar**: Navigation links (Dashboard, OKR Management, Team Management, etc.).
- **Main Content**: Real-time performance metrics, progress visualizations, quick links to recent OKR sessions.
- **Footer**: Quick access to support and documentation.

### Profile
- **Header**: Back to dashboard link.
- **Profile Information**: User details, edit option.
- **Settings**: Notification preferences, security settings.

### Login/Register
- **Login Form**: Email and OTP entry.
- **Register Form**: Multi-step process for new users.
- **Access Code Input**: Initial step for invite-only access.

### OKR Management
- **Header**: Create new OKR button.
- **OKR List**: Table view with hierarchical structure, progress indicators.
- **Detail Modal**: CRUD operations for selected OKR.

### Team Management
- **Header**: Add new team button.
- **Team List**: Table view with team details, member count.
- **Detail Modal**: Team member management, role assignments.

### Session Management
- **Session List**: Cards with session status (Open, In Progress, Archived).
- **Session Detail**: Timeline view of session progress, key milestones.

### Reports & Analytics
- **Filter Options**: By session, team, user, confidence levels.
- **Charts**: Progress over time, team performance rollup.
- **Export Options**: CSV, JSON formats.

### Admin Settings
- **Organization Management**: Invite new users, manage roles.
- **System Settings**: Integration endpoints, notification schedules.

### Notifications
- **List View**: Recent notifications with type (progress update, goal completion).
- **Settings**: Manage notification preferences.

### Help/Support
- **FAQs**: Common questions and answers.
- **Contact Form**: Submit support requests.

## UI Components
- **Buttons**: Primary, secondary, icon buttons.
- **Modals**: Detail view, confirmation dialogs.
- **Forms**: Input fields, dropdowns, radio buttons.
- **Cards**: Information display, session overview.
- **Tables**: Data presentation with sorting/filtering.
- **Charts**: Line, bar, pie charts using Recharts.
- **Navigation Bar**: Collapsible sidebar with icons.
- **Progress Indicators**: Bars, percentages, confidence levels.

## Navigation Structure
- **Routing Flow**: 
  - Home → Login/Register → Dashboard
  - Dashboard → OKR Management, Team Management, etc.
- **Menu Items**: 
  - Dashboard, OKR Management, Team Management, Session Management, Reports & Analytics, Admin Settings, Notifications, Help/Support.
- **Navigation Patterns**: 
  - Collapsible sidebar for main navigation.
  - Top bar for profile and settings access.

## Color Scheme & Fonts
- **Primary Colors**: 
  - #1A202C (Dark Gray)
  - #E53E3E (Red)
  - #38B2AC (Teal)
- **Secondary Colors**: 
  - #EDF2F7 (Light Gray)
  - #F7FAFC (White)
- **Typography**: 
  - Font Family: Geist Sans
  - Headings: Bold, size varies by level
  - Body Text: Regular, 14px

## User Flow
1. **New User Registration**:
   - Access code entry → Organization setup → OTP verification → Profile completion.
2. **Login**:
   - Email entry → OTP verification → Redirect to Dashboard.
3. **OKR Creation**:
   - Navigate to OKR Management → Click "Create New" → Enter details → Assign owners → Save.
4. **Progress Update**:
   - Navigate to OKR detail → Enter progress → Save updates.

## Responsiveness
- **Mobile-First Approach**: 
  - Design starts with mobile layout, scales to larger screens.
- **Breakpoint Rules**: 
  - Small devices: Up to 640px
  - Medium devices: 641px to 768px
  - Large devices: 769px and above
- **Adaptive Layouts**: 
  - Sidebar collapses on mobile, expands on larger screens.
  - Charts and tables adjust to screen size, maintaining readability.

## State Management
- **Approach**: 
  - Using React Context API for global state management.
  - Local state managed within components for specific interactions.
- **Context**: 
  - User Authentication Context
  - OKR Data Context
  - Notification Context
- **Data Fetching**: 
  - Supabase Realtime for live updates.
  - REST API calls for fetching and updating data.