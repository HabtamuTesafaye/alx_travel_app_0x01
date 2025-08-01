# alx_travel_app_0x01

A Django RESTful API for managing travel listings, bookings, and reviews. This project is designed to provide a backend for a travel application, supporting user authentication, listing management, booking operations, and review submissions.

---

## Features

- **User Authentication**: Secure registration and login using Django's built-in user model and token authentication.
- **Listings**: CRUD operations for travel listings (e.g., hotels, apartments, experiences).
- **Bookings**: Users can book listings, view their bookings, and manage (change/cancel) them.
- **Reviews**: Users can leave reviews and ratings for listings.
- **Permissions**: Fine-grained permissions for viewing, adding, changing, and deleting listings, bookings, and reviews.
- **Browsable API**: Interactive API documentation via Swagger and Redoc.

---

## API Endpoints

All endpoints are prefixed by `/listings/` (as included in your main project URLs).

| Resource   | Endpoint                  | Methods         | Description                |
|------------|---------------------------|-----------------|----------------------------|
| Listings   | `/listings/`              | GET, POST       | List or create listings    |
| Listings   | `/listings/{id}/`         | GET, PUT, PATCH, DELETE | Retrieve, update, or delete a listing |
| Bookings   | `/bookings/`              | GET, POST       | List or create bookings    |
| Bookings   | `/bookings/{id}/`         | GET, PUT, PATCH, DELETE | Retrieve, update, or delete a booking |
| Reviews    | `/reviews/`               | GET, POST       | List or create reviews     |
| Reviews    | `/reviews/{id}/`          | GET, PUT, PATCH, DELETE | Retrieve, update, or delete a review |

> **Note:** Authentication is required for most operations.

---

## Setup & Installation

1. **Clone the repository:**
    ```bash
    git clone <repo-url>
    cd alx_travel_app_0x01
    ```

2. **Create and activate a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Apply migrations:**
    ```bash
    python manage.py migrate
    ```

5. **Create a superuser (admin):**
    ```bash
    python manage.py createsuperuser
    ```

6. **Run the development server:**
    ```bash
    python manage.py runserver
    ```

---

## API Documentation

- **Swagger UI:** [http://localhost:8000/swagger/](http://localhost:8000/swagger/)
- **Redoc:** [http://localhost:8000/redoc/](http://localhost:8000/redoc/)

---

## Project Structure

```
alx_travel_app_0x01/
├── alx_travel_app/
│   ├── listings/
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── serializers.py
│   │   ├── urls.py
│   │   └── ...
│   ├── db.sqlite3
│   ├── settings.py
│   ├── urls.py
│   └── ...
├── manage.py
└── README.md
```

---

## Permissions & Roles

The app uses Django's permission system. Example permissions include:

- `add_listing`, `change_listing`, `delete_listing`, `view_listing`
- `add_booking`, `change_booking`, `delete_booking`, `view_booking`
- `add_review`, `change_review`, `delete_review`, `view_review`

Assign these permissions to users or groups as needed via the Django admin.

---

