# SchoolHub

A central dashboard for students to track schedules, assignments, and school information.

## Overview

SchoolHub is a comprehensive web application built with Flask that serves as a central hub for students to manage their academic life. It combines essential tools including a dashboard, calendar, task manager, and bulletin board in one intuitive interface.

## Features

### Dashboard
- Live-updating clock with seconds
- Current weather information
- Daily inspirational quote
- School bulletin board with important announcements

### Calendar
- Monthly calendar view
- Daily event listing
- Event details with location and time
- Visual indicators for important dates

### Task Management
- Course-based task organization
- Due date tracking
- Task completion status
- Add/remove tasks with persistent storage

### User Experience
- Responsive design for all devices
- Dark/light mode toggle
- Customizable settings
- Intuitive navigation

### Admin Features
- Bulletin management system
- Content moderation tools
- User account management

## Tech Stack

- **Backend**: Python with Flask
- **Frontend**: HTML, CSS with minimal JavaScript
- **Database**: Supabase for data storage
- **Authentication**: Supabase Auth (Google/Apple login)
- **Deployment**: Render

## Installation

### Prerequisites
- Python 3.8+
- pip
- virtualenv (recommended)

### Setup

1. Clone the repository
```bash
git clone https://github.com/yourusername/schoolhub.git
cd schoolhub
```

2. Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Set up environment variables
Create a `.env` file in the project root with the following variables:
```
SECRET_KEY=your_secret_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
WEATHER_API_KEY=your_weather_api_key
FLASK_ENV=development
```

5. Run the application
```bash
python app.py
```

6. Open your browser and navigate to `http://localhost:5000`

## Project Structure

```
schoolhub/
├── app.py                  # Main Flask application
├── config.py               # Configuration settings
├── requirements.txt        # Dependencies
├── static/                 # Static assets
│   ├── css/                # CSS files
│   ├── js/                 # JavaScript files
│   └── images/             # Image files
├── templates/              # Jinja2 templates
│   ├── base.html           # Base template
│   ├── components/         # Reusable components
│   ├── dashboard/          # Dashboard screen
│   ├── calendar/           # Calendar screen
│   ├── tasks/              # Tasks screen
│   ├── settings/           # Settings screen
│   ├── admin/              # Admin pages
│   └── auth/               # Authentication pages
├── models/                 # Data models
│   ├── user.py             # User model
│   ├── task.py             # Task model
│   └── bulletin.py         # Bulletin model
└── routes/                 # Route definitions
    ├── main.py             # Main routes
    ├── auth.py             # Authentication routes
    ├── api.py              # API endpoints
    └── admin.py            # Admin routes
```

## Development

### Adding a New Page

1. Create a new template in the appropriate directory under `templates/`
2. Add a new route in the corresponding route file under `routes/`
3. Update the navigation in `base.html` if needed

### Styling

- The application uses Tailwind CSS for styling
- Dark mode is supported through CSS classes and theme switching

## Deployment

### Deploying to Render

1. Create a new Web Service on Render
2. Link your GitHub repository
3. Set the build command: `pip install -r requirements.txt`
4. Set the start command: `gunicorn app:app`
5. Add your environment variables
6. Deploy!

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Open a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

Built with ❤️ for better student organization
