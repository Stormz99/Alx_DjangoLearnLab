# Social Media API - Foundation Setup

## Project Description
This Django REST Framework project provides the foundation for a social media API with user authentication

## Features
- Custom User model extending AbstractUser
- Token-based authentication
- User registration and login endpoints
- User profile management

## User Model Fields
- username, email, password (from AbstractUser)
- bio: Text field for user biography (max 500 characters)
- profile_picture: Char field for image path/URL
- followers: Many-to-many self-referential relationship

## API Endpoints
- `POST /api/auth/register/` - Register new user (returns token)
- `POST /api/auth/login/` - Login user (returns token)  
- `GET /api/auth/profile/` - Get user profile (requires authentication)
- `PUT /api/auth/profile/` - Update user profile (requires authentication)

## Setup
1. Install dependencies: `pip install -r requirements.txt`
2. Run migrations: `python manage.py migrate`
3. Create superuser: `python manage.py createsuperuser`
4. Run server: `python manage.py runserver`

## Testing
The foundation has been tested and verified:
- Custom user model creates users successfully
- Serializers validate data correctly
- All components are properly integrated

## Authentication
Uses Django REST Framework Token Authentication. Include in headers:
`Authorization: Token <your_token_here>`
# Alx_DjangoLearnLab
