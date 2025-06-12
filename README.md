# Event Management System

A modern, responsive event management platform built with React, TypeScript, and Tailwind CSS.

## Features

- **Authentication System**: Role-based access with Admin and User roles
- **Event Discovery**: Browse and search events with advanced filtering
- **Event Management**: Create, edit, and delete events (Admin only)
- **User Dashboard**: Track registered events and manage organized events
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Demo Accounts

### Admin Account
- **Email**: `admin@eventhub.com`
- **Password**: `admin123`
- **Permissions**: Can create, edit, and delete events

### User Accounts
- **Email**: `user@example.com` | **Password**: `user123`
- **Email**: `jane@example.com` | **Password**: `jane123`
- **Permissions**: Can browse and register for events

## Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (version 16 or higher)
- **npm** or **yarn** package manager

## Installation & Setup

1. **Clone or Download the Project**
   ```bash
   # If using git
   git clone <repository-url>
   cd event-management-system
   
   # Or download and extract the ZIP file
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Start the Development Server**
   ```bash
   npm run dev
   ```

4. **Open in Browser**
   - The application will be available at `http://localhost:5173`
   - Use one of the demo accounts above to log in

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Project Structure

```
src/
├── components/          # React components
│   ├── Header.tsx      # Navigation header
│   ├── LoginForm.tsx   # Authentication form
│   ├── EventGrid.tsx   # Event listing grid
│   ├── EventCard.tsx   # Individual event card
│   ├── FilterSidebar.tsx # Event filtering
│   ├── CreateEventForm.tsx # Event creation form
│   └── Dashboard.tsx   # User dashboard
├── data/               # Mock data
│   └── mockData.ts     # Sample events and users
├── types/              # TypeScript definitions
│   └── index.ts        # Type definitions
├── App.tsx             # Main application component
├── main.tsx           # Application entry point
└── index.css          # Global styles
```

## Key Features Explained

### Authentication
- Hardcoded user authentication for demo purposes
- Role-based access control (Admin vs User)
- Secure login/logout functionality

### Event Management
- **Admins** can create, edit, and delete events
- **Users** can browse and register for events
- Rich event details with images, categories, and tags

### Responsive Design
- Mobile-first approach using Tailwind CSS
- Adaptive layouts for different screen sizes
- Touch-friendly interface elements

## Technology Stack

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling framework
- **Lucide React** - Icon library
- **Vite** - Build tool and dev server

## Customization

### Adding New Event Categories
Edit `src/types/index.ts` and add new categories to the `EventCategory` type:

```typescript
export type EventCategory = 
  | 'workshop' 
  | 'seminar' 
  | 'festival' 
  | 'webinar' 
  | 'meetup' 
  | 'conference' 
  | 'networking'
  | 'your-new-category'; // Add here
```

### Modifying User Roles
Update the authentication system in `src/data/mockData.ts` to add new users or modify existing ones.

### Styling Changes
The project uses Tailwind CSS. Modify classes in components or extend the configuration in `tailwind.config.js`.

## Production Deployment

1. **Build the project**:
   ```bash
   npm run build
   ```

2. **Deploy the `dist` folder** to your hosting provider (Netlify, Vercel, etc.)

## Support

This is a demo application with hardcoded authentication. For production use, you would need to:

- Implement real authentication (JWT, OAuth, etc.)
- Add a backend API for data persistence
- Implement proper error handling and validation
- Add automated testing

## License

This project is for educational and demonstration purposes.