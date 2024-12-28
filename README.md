# Startup Social Platform

## Project Description

This project is a social platform designed for startups and entrepreneurs to connect, share ideas, and collaborate. Users can create profiles, share posts, like and comment on posts, and send messages. The platform also supports startup creation, allowing users to join or manage startups, with roles and other relevant information.

The platform uses Laravel as the backend framework, providing a structured way to manage authentication, database models, and relationships. This project also includes various features such as post sharing, messaging systems, and industry management for startups.

## Project Structure

```plaintext
├── app/
│   └── Models/
│       ├── Comment.php        - Model for handling comments on posts
│       ├── Message.php        - Model for handling messages between users
│       ├── Post.php           - Model for handling posts made by users
│       ├── PostLike.php       - Model for handling likes on posts
│       ├── Startup.php        - Model for handling startup information
│       ├── StartupMember.php  - Model for handling users as members of startups
│       └── User.php           - Model for handling user information and relationships
├── database/
│   └── migrations/           - Migration files for creating tables related to the models (e.g., users, posts, comments, etc.)
├── resources/
│   └── views/                - Blade templates for front-end (views for the user dashboard, posts, profile, etc.)
└── routes/
    └── web.php               - API and web routes for managing various endpoints for posts, comments, messages, startups, etc.
```

## Technologies and Frameworks used

**Backend**: Laravel 12
**Database**: MySQL
**Authentication**: Laravel built-in authentication system
**Relationships**: Eloquent ORM for managing relationships (e.g., hasMany, belongsTo)

## Setup and Run instructions

### Prerequisites

PHP 8.0+ (preferably 8.2)
Composer
MySQL or any supported relational database

### Steps

**1. Clone the repository**

```plaintext
git clone https://github.com/yourusername/your-repository.git
cd your-repository
```

**2. Install Backend dependencies**

```plaintext
composer install
```

**3. Setup environment file**

```plaintext
cp .env.example .env
```

**4. Generate application key**

```plaintext
php artisan key:generate
```

**5. Run migrations**

```plaintext
php artisan migrate
```

**6. Run application**

```plaintext
php artisan serve
```

## Deployment links

**Live Demo:** [Insert link here]

## Documented Features

**1. User Management**

Sign Up/Sign In: Users can register or log in using basic credentials.
User Profile: Includes fields for Username, Email, Bio, and link to their associated startup (with position/title).

**2. Startup Profile**

Startup Creation: Users can create and manage startup organizations.
Profile Details: Includes Logo, Name, Description, Industries, and Funding Raised.
Timeline Feature: Hardcoded and customizable milestones.

Sections:

- Posts Section
- Employee Section (roles and positions)
- Project Portfolio (for service-based startups)
- Product Showcase (for product-based startups)
- Hybrid Section (both Portfolio and Showcase for hybrid startups).

**3. Feed**

Post Creation: Users can create posts with optional image attachments and Markdown formatting.
Interactions: Like, comment, save, and share posts.
Feed Visibility: Public visibility, allowing even anonymous users to view posts.

**4. Search**

Startup Search: Filter by Industry Type and Location.

**5. Messaging**

Allows users to send private messages to others and share posts.

**6. Sharable Profiles and Posts**

User, startup, and post profiles have unique, shareable URLs.

**7. Organization Management**

Users can join startups and have different roles:
Owner: Manages invites and requests.
Editor: Can create posts and manage content.
Viewer: Read-only access.
Employee Section: Displays users with their roles and positions.

**8. Subscriptions and Notifications**

Automatic Subscriptions: Users are auto-subscribed to organizations they belong to.
Optional Subscriptions: Users can follow other startups for updates.

**9. Event Management**

Event Creation: Special post type for events with detailed information (Title, Description, Start/End time, Location).
Event Display: Events appear in profiles and feeds.
Event Subscription: Users can RSVP and receive notifications.
Event Attendees: Lists attendees and headcount.
