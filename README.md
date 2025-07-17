# Inventory Management System

A Django-based web application for managing product inventory with full CRUD (Create, Read, Update, Delete) functionality.

## Features

- **Product Management**: Add, view, edit, and delete products
- **Product Information**: Track product name, SKU, price, quantity, and supplier
- **Responsive Design**: Built with Bootstrap 4.5.2 for mobile-friendly interface
- **User-Friendly Interface**: Clean and intuitive web interface
- **Navigation**: Easy-to-use navigation menu with toggle support for mobile devices

## Technology Stack

- **Backend**: Django (Python web framework)
- **Frontend**: HTML5, CSS3, Bootstrap 4.5.2
- **Database**: SQLite (default Django database)
- **Forms**: Django Crispy Forms with Bootstrap styling
- **Python Version**: 3.13

## Project Structure

```
FinalProject/
├── Pipfile                 # Python dependencies
├── Pipfile.lock           # Locked dependencies
├── README.md              # This file
└── invProject/            # Django project root
    ├── db.sqlite3         # SQLite database
    ├── manage.py          # Django management script
    ├── invApp/            # Main application
    │   ├── __init__.py
    │   ├── admin.py       # Django admin configuration
    │   ├── apps.py        # App configuration
    │   ├── forms.py       # Django forms
    │   ├── models.py      # Database models
    │   ├── tests.py       # Unit tests
    │   ├── urls.py        # URL routing
    │   ├── views.py       # View controllers
    │   ├── migrations/    # Database migrations
    │   └── templates/     # HTML templates
    │       └── invApp/
    │           ├── home.html
    │           ├── layout.html
    │           ├── product_confirm_delete.html
    │           ├── product_form.html
    │           └── product_list.html
    └── invProject/        # Django project settings
        ├── __init__.py
        ├── asgi.py        # ASGI configuration
        ├── settings.py    # Project settings
        ├── urls.py        # Main URL configuration
        └── wsgi.py        # WSGI configuration
```

## Installation & Setup

### Prerequisites

- Python 3.13 or higher
- pip (Python package installer)
- pipenv (for virtual environment management)

### Installation Steps

1. **Clone or download the project**

   ```bash
   cd FinalProject
   ```

2. **Install dependencies using pipenv**

   ```bash
   pipenv install
   ```

3. **Activate the virtual environment**

   ```bash
   pipenv shell
   ```

4. **Navigate to the Django project directory**

   ```bash
   cd invProject
   ```

5. **Run database migrations**

   ```bash
   python manage.py migrate
   ```

6. **Create a superuser (optional, for admin access)**

   ```bash
   python manage.py createsuperuser
   ```

7. **Start the development server**

   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your web browser
   - Navigate to `http://127.0.0.1:8000/` or `http://localhost:8000/`

## Usage

### Main Features

1. **Home Page**: Welcome page with navigation to main features
2. **Add Product**: Create new products with the following fields:

   - Product Name
   - SKU (Stock Keeping Unit)
   - Price
   - Quantity
   - Supplier

3. **Product List**: View all products in a responsive table format
4. **Edit Product**: Update existing product information
5. **Delete Product**: Remove products from inventory with confirmation

### Navigation

- **Home**: Return to the main dashboard
- **Add Product**: Navigate to the product creation form
- **Product List**: View all products in the inventory

## Database Schema

### Product Model

| Field      | Type         | Description                   |
| ---------- | ------------ | ----------------------------- |
| product_id | AutoField    | Primary key (auto-increment)  |
| name       | CharField    | Product name (max 100 chars)  |
| sku        | CharField    | Unique SKU (max 50 chars)     |
| price      | FloatField   | Product price                 |
| quantity   | IntegerField | Stock quantity (default: 0)   |
| supplier   | CharField    | Supplier name (max 100 chars) |

## Development

### Dependencies

- **Django**: Web framework
- **django-crispy-forms**: Enhanced form rendering
- **crispy-bootstrap5**: Bootstrap 5 styling for forms

### Key Files

- `models.py`: Database model definitions
- `views.py`: Business logic and request handling
- `forms.py`: Django form definitions
- `urls.py`: URL routing configuration
- `templates/`: HTML templates with Bootstrap styling
