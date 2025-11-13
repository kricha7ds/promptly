# Promptly

An AI-powered word puzzle game inspired by Reddit's Syllo. Instead of receiving the same daily puzzle as everyone else, users provide their own prompts and AI generates personalized word puzzles with scrambled pieces to solve.

## Tech Stack

- **Backend**: Ruby on Rails 7.2.3
- **Frontend**: Vue.js 3.5
- **Styling**: Tailwind CSS v4
- **Build Tool**: Vite (with Hot Module Replacement)
- **Ruby Version**: 3.2.2

## Prerequisites

- Ruby 3.2.2
- Rails 7.2.3
- Node.js (for npm)
- Bundler
- PostgreSQL 14+ (15.8 recommended)

## Getting Started

### Installation

1. Clone the repository:

```bash
git clone <repo-url>
cd promptly
```

2. Install Ruby dependencies:

```bash
bundle install
```

3. Install JavaScript dependencies:

```bash
npm install
```

4. Set up the databases:

```bash
rails db:create
```

### Running the App

Start the development server:

```bash
bin/dev
```

This command starts:

- Rails server on port `3000`
- Vite dev server with HMR (Hot Module Replacement)

Visit `http://localhost:3000` to see the app.

### Development

The app uses Vite for fast development with instant Hot Module Replacement:

- Changes to Vue components update instantly without page refresh
- Tailwind CSS changes are applied immediately
- Full page reload only happens when necessary

### Project Structure

```
app/
├── javascript/
│   ├── entrypoints/
│   │   └── application.js    # Main JS entry point
│   └── App.vue                # Root Vue component
├── assets/
│   └── stylesheets/
│       └── application.tailwind.css  # Tailwind CSS imports
└── views/
    └── layouts/
        └── application.html.erb  # Main layout
```

## How It Works

1. User provides a custom prompt (e.g., "space exploration terms")
2. AI generates related words with definitions
3. Words are broken into scrambled syllable pieces
4. User solves the puzzle by matching definitions to words using the pieces

## Contributing

This project is in early development. If you're interested in contributing, please reach out or open an issue to discuss potential changes.

## License

TBD
