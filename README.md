# Quizio - Quiz Game Project

## Overview

This project is a web-based quiz game built with HTML, CSS, and JavaScript on the frontend and Django on the backend. The quiz dynamically fetches questions from the server, calculates scores, and displays results interactively. The project demonstrates a fully integrated frontend and backend setup.

## Features 

-Interactive Quiz Gameplay: Users can answer multiple-choice questions and get real-time feedback.

-Dynamic Question Loading: Questions are fetched from the server using Django views.

-Result Display: Shows the final score and a graphical representation of the user's performance.

-Responsive Design: Works seamlessly on different screen sizes.

-Easy to Extend: Add more questions or customize the game logic easily.

## Key Files

-static/quiz/style.css: Contains all styles for the quiz.

-static/quiz/script.js: Manages the quiz logic and interactivity.

-templates/quiz/index.html: Main HTML file for the quiz page.

-views.py: Django view functions to render templates and serve data.

-urls.py: URL mappings for the quiz application.

## Setup Instructions 

### Prerequisites

-Python 3.x

-Django 4.x

-A web browser

# Installation Steps 

1. Clone the Repository:
```
git clone <repository-url>
cd quiz
```
2. Set Up a Virtual Environment:
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install Dependencies:
```
pip install django
```
4. Configure the Database:

    - Run migrations to set up the default database:
```
python manage.py makemigrations
python manage.py migrate
```
Run the Development Server:
```
python manage.py runserver
```
Access the Application:

Open your browser and navigate to:
```
http://127.0.0.1:8000
```
## Configuration

### Static Files

Ensure the following settings are in your settings.py to serve static files correctly:
```
STATIC_URL = '/static/'
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, "quiz", "static"),
]
STATIC_ROOT = os.path.join(BASE_DIR, "staticfiles")
```
### Templates

Add the path to the templates directory in your settings.py:
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR, 'quiz', 'templates')],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
```
## Usage 

Start the quiz by clicking the Start Quiz button on the home page.

Answer the questions presented in the quiz.

View your score and results at the end.

Retry the quiz or navigate back to the home page.
