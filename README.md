
```markdown
# DRF Todo app

## Project Overview
- A simple task management API built with Django REST Framework.
- Provides endpoints for managing tasks, users, and authentication.
- Implements token-based authentication.

## Features
- User registration and authentication.
- CRUD operations for tasks.
- Token-based authentication using Django REST Framework's `authtoken`.
- Pagination and filtering for task lists.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/kenethoriga/drf-task-app.git
   cd drf-task-manager
   ```



2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Apply migrations**:
   ```bash
   python manage.py migrate
   ```

4. **Create a superuser**:
   ```bash
   python manage.py createsuperuser
   ```

5. **Run the development server**:
   ```bash
   python manage.py runserver
   ```

## API Endpoints

- **User Registration**: `/api/sigup/` (POST)
- **User Login**: `/api/login/` (POST)
- **Task List**: `/api/todo/` (GET, POST)
- **Task Detail**: `/api/todo/<id>/` (GET, PUT, DELETE)

## Usage

1. **Register a new user**:
   ```http
   POST /api/register/
   {
       "username": "yourusername",
       "password": "yourpassword"
   }
   ```

2. **Obtain an authentication token**:
   ```http
   POST /api/login/
   {
       "username": "yourusername",
       "password": "yourpassword"
   }
   ```

3. **Use the token to authenticate requests**:
   - Add the following header to your requests:
     ```
     Authorization: Token yourtoken
     ```

4. **Create a new task**:
   ```http
   POST /api/tasks/
   {
       "title": "New Task",
       "description": "Task description"
   }
   ```

## Project Structure

- **api/**: Contains the Django app for the API.
  - `models.py`: Database models.
  - `views.py`: API views.
  - `serializers.py`: DRF serializers.
  - `urls.py`: URL routing.
- **backend/**: Contains project settings and configurations.
  - `settings.py`: Django settings.
  - `urls.py`: Root URL configurations.
- **requirements.txt**: List of dependencies.

## Contributing
- Fork the repository.
- Create a new branch (`git checkout -b feature-branch`).
- Make your changes and commit them (`git commit -m 'Add new feature'`).
- Push to the branch (`git push origin feature-branch`).
- Create a pull request.

## License
- This project is licensed under the MIT License.

## Contact
- For any questions or suggestions, please open an issue or contact `kenethoriga@live.com`.
```
