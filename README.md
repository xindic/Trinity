# Startup Social Platform

## Overview

The **Startup Social Platform** is a scalable and modular web application designed to facilitate startup collaboration, networking, and growth. Tailored for startup teams and entrepreneurs, the platform enables users to create and manage startup profiles, engage with content through posts and messages, explore other startups, and access advanced features like subscriptions, event management, and calendar integration.

Over a three-day development cycle, core functionalities were implemented to support user interactions, startup management, and communication, with additional features for enhanced organization, event handling, and integrations.

## Project Structure

```plaintext
├── app/                    # Application core files (Controllers, Models, etc.)
├── bootstrap/               # Framework bootstrap files
├── config/                  # Application configuration files
├── database/                # Database migrations and seeders
├── public/                  # Public files (assets, images, etc.)
├── resources/               # Views and assets
│   ├── views/               # Blade template views
│   ├── js/                  # JavaScript files
│   └── css/                 # Stylesheets
├── routes/                  # Web and API routes
├── storage/                 # Storage files (logs, file uploads, etc.)
├── tests/                   # Automated tests
├── .env                     # Environment configuration
├── composer.json            # Composer dependencies
├── package.json             # Node.js dependencies
└── README.md                # Project documentation
```

## Technologies and Frameworks used

**Backend**: Laravel 10
**Frontend**: Blade, Tailwind CSS, AlpineJS
**Database**: MySQL
**Authentication**: Laravel Breeze for authentication
**Real-time** Communication: Laravel Echo and Pusher
**File Storage**: Laravel's built-in file storage for images and documents

## Setup and Run instructions

**1. Clone the repository**
git clone <repository-url>
cd startup-social-platform

**2. Install Backend dependencies**
composer install

**3. Install Frontend dependencies**
npm install
npm run dev

**4. Setup environment file**
cp .env.example .env

**5. Generate application key**
php artisan key:generate

**6. Run migrations**
php artisan migrate

**7. Run application**
php artisan serve

## Deployment links

**Live Demo:** [Insert link here]

## Documented Features

1. User Management

   Sign Up/Sign In: Users can register or log in using basic credentials.
   User Profile:
   Includes fields for Username, Email, Bio, and link to their associated startup (with position/title).

2. Startup Profile

   Startup Creation: Users can create and manage startup organizations.
   Profile Details: Includes Logo, Name, Description, Industries, and Funding Raised.
   Timeline Feature: Hardcoded and customizable milestones (e.g., "Founded", "First Funding Round").
   Sections:
   Posts Section
   Employee Section (roles and positions)
   Project Portfolio (for service-based startups)
   Product Showcase (for product-based startups)
   Hybrid Section (both Portfolio and Showcase for hybrid startups).

3. Feed

   Post Creation: Users can create posts with optional image attachments and Markdown formatting.
   Interactions: Like, comment, save, and share posts.
   Feed Visibility: Public visibility, allowing even anonymous users to view posts.

4. Search

   Startup Search: Filter by Industry Type and Location.
   Anonymous Mode: Users can browse but cannot interact (comment, message, etc.).

5. Messaging

   Direct Messaging: Allows users to send private messages to others and share posts.
   Restrictions: Messaging is not available for anonymous users.

6. Sharable Profiles and Posts

   User, startup, and post profiles have unique, shareable URLs.

7. Organization Management

   Users can join startups and have different roles:
   Owner: Manages invites and requests.
   Editor: Can create posts and manage content.
   Viewer: Read-only access.
   Employee Section: Displays users with their roles and positions.

8. Subscriptions and Notifications

   Automatic Subscriptions: Users are auto-subscribed to organizations they belong to.
   Optional Subscriptions: Users can follow other startups for updates.

9. Event Management

   Event Creation: Special post type for events with detailed information (Title, Description, Start/End time, Location).
   Event Display: Events appear in profiles and feeds.
   Event Subscription: Users can RSVP and receive notifications.
   Event Attendees: Lists attendees and headcount.

10. Calendar Integration

    Export: Users can export events to .ics format.
    Sync: Events can be directly synced with Google Calendar and Outlook.
