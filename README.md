# Recipe Finder

A web-based Recipe Finder app that allows users to search for recipes based on ingredients or keywords, with additional filters for mood and estimated cooking time. The app fetches recipes using the [MealDB API](https://www.themealdb.com/) and provides a user-friendly interface for quick recipe browsing.

## Features
- **Recipe Search**: Find recipes by name or keyword.
- **Mood Filter**: Filter recipes based on mood (Comfort, Refreshing, Hearty).
- **Time Filter**: Filter recipes by maximum estimated cooking time.
- **Load More**: Dynamically load more recipes for broader options.

## Technologies
- **Frontend**: React, TailwindCSS
- **API**: [MealDB API](https://www.themealdb.com/) for recipe data
- **Icons**: `react-icons`

## Setup Instructions

### 1. Prerequisites
- **Node.js**: Ensure you have Node.js installed on your machine. You can download it from [Node.js](https://nodejs.org/).
- **API Key**: The MealDB API is free to use and doesn’t require an API key for the public search functions.

### 2. Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/recipe-finder.git
   cd recipe-finder
Install the required dependencies:

bash
Copy code
npm install
Start the development server:

bash
Copy code
npm start
Open your browser and navigate to http://localhost:3000.

Project Structure
php
Copy code
.
├── public              # Static assets
├── src
│   ├── components      # React components
│   │   ├── SearchBar.js        # Search bar component
│   │   ├── RecipeCard.js       # Recipe card component for displaying each recipe
│   │   ├── Button.js           # Reusable button component
│   │   ├── Loader.js           # Loading spinner
│   │   └── Recipes.js          # Main Recipes component with filtering logic
│   ├── utils
│   │   ├── index.js            # Utility functions for mood and time categorization
│   ├── App.js                  # Main app component
│   └── index.js                # Entry point
├── README.md                   # Project documentation
└── package.json                # Project configuration and dependencies
Usage
Search for Recipes
Enter a keyword in the search bar (e.g., "Vegan," "Chicken," "Cake").
Click the search icon or press Enter to search for recipes.
Filter by Mood and Time
Mood Filter: Select a mood from the dropdown (Comfort, Refreshing, Hearty). Recipes will update based on the mood selection.
Time Filter: Select the maximum cooking time (in minutes) from the dropdown (15, 30, 45, or 60). Recipes will be filtered to match the selected time range.
Load More Recipes
Click the Show More button at the bottom to load additional recipes.

Custom Filtering Logic
Since MealDB API does not natively support filtering by mood and time, custom utility functions in utils/index.js help categorize recipes as follows:

Mood: Recipes are tagged with moods (Comfort, Refreshing, Hearty) based on keywords in the recipe name, category, or ingredients.
Time: The estimated cooking time is determined based on instructions or default assumptions, allowing filtering by user-selected time limits.

