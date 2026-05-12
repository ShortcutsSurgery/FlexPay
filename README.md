# FlexPay

FlexPay is a map-centric local job marketplace designed to connect local businesses with workers seeking hourly-based shifts. It features real-time location accuracy, transparent pay calculations, and a robust shift management system.

## Features

- **Map-Centric Interface**: Find local jobs on an interactive map.
- **Dynamic Pay Calculator**: Automatic handling of night shift premiums (1.5x) and short-notice bonuses.
- **GPS Check-in**: Secure shift timer with location verification.
- **Real-Time Tracking**: Earnings dashboard for workers and labor cost breakdowns for employers.

## Tech Stack

- **Frontend**: React, Leaflet, Framer Motion, Tailwind CSS
- **Backend**: FastAPI, MongoDB, JWT Authentication
- **Payments**: Stripe Integration

## Getting Started

### Prerequisites

- Node.js (v18+)
- Python (v3.10+)
- MongoDB (local or Atlas)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ShortcutsSurgery/FlexPay.git
   cd FlexPay
   ```

2. **Backend Setup:**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
   Create a `.env` file in the `backend` directory:
   ```env
   MONGO_URL=mongodb://localhost:27017
   DB_NAME=flexpay
   JWT_SECRET=your_secret_key
   STRIPE_SECRET_KEY=your_stripe_test_key
   ```

3. **Frontend Setup:**
   ```bash
   cd ../frontend
   yarn install  # or npm install
   ```
   Create a `.env` file in the `frontend` directory:
   ```env
   REACT_APP_API_URL=http://localhost:8001/api
   ```

### Running the App

1. **Start the Backend:**
   ```bash
   cd backend
   uvicorn server:app --reload --port 8001
   ```

2. **Start the Frontend:**
   ```bash
   cd ../frontend
   yarn start
   ```

The app will be available at `http://localhost:3000`.