# SmartServe

SmartServe is an on-demand home service booking and management platform built using Flask and MongoDB. It connects customers looking for home services (plumbing, electrical work, cleaning, repairs, etc.) with verified local service providers.

---

## Features

### User Portal
- **User Authentication**: Secure signup and login.
- **Provider Discovery**: Browse and filter verified service providers by category and location.
- **Provider Profiles**: View provider credentials, hourly rates, experience, and customer reviews.
- **Slot Booking**: Schedule appointments based on provider availability.
- **Payment & Booking Management**: Track booking statuses and view payment receipts.

### Service Provider Portal
- **Registration & Verification**: Register with certificate and qualification document uploads.
- **Schedule Management**: Create and manage available time slots.
- **Job Tracking**: View assigned jobs, update status to completed, and manage client requests.

### Admin Portal
- **Verification Desk**: Review and approve/reject provider registrations and uploaded certificates.
- **User Management**: View and manage customer accounts.
- **Provider Management**: Monitor active service providers.
- **Bookings & Payments Overview**: Track all service bookings and financial transactions.

---

## Tech Stack

- **Backend**: Python 3.x, Flask, PyMongo, Gunicorn, Werkzeug
- **Database**: MongoDB
- **Frontend**: HTML5, CSS3, JavaScript, Jinja2 Templates

---

## Project Structure

```text
smartserve/
├── backend/
│   ├── app.py              # Main Flask application server
│   ├── database.py         # MongoDB connection setup and collections
│   ├── Procfile            # Deployment script for Heroku/Render
│   └── static/
│       └── uploads/        # Provider certificates and static assets
├── frontend/
│   └── templates/
│       ├── admin/          # Admin dashboard templates
│       ├── auth/           # Login & Registration templates
│       ├── provider/       # Provider dashboard & schedule templates
│       └── user/           # User search, booking, & profile templates
├── .gitignore              # Ignored files (virtual environment, cache, etc.)
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

---

## Getting Started

### Prerequisites

Ensure you have the following installed on your machine:
- [Python 3.8+](https://www.python.org/downloads/)
- [MongoDB Community Server](https://www.mongodb.com/try/download/community) (running locally on port `27017`) or a [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) URI.

---

### Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Swat-hy/smartserve.git
   cd smartserve
   ```

2. **Create and Activate a Virtual Environment**
   - **Windows:**
     ```bash
     python -m venv venv
     .\venv\Scripts\activate
     ```
   - **macOS/Linux:**
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Start MongoDB**
   Make sure your local MongoDB server is running on `mongodb://localhost:27017/`.

5. **Run the Application**
   ```bash
   python backend/app.py
   ```

6. **Access in Browser**
   Open your browser and navigate to:
   ```text
   http://127.0.0.1:5000/
   ```

---

## Default Credentials

- **Admin Login:**
  - **Email:** `admin@gmail.com`
  - **Password:** `admin123`

---

## License

This project is open-source and available under the MIT License.
