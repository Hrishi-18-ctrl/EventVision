# EventVision

EventVision is an AI-powered Event Gallery System that allows event organizers to upload event photos and enables guests to find their own images using face recognition technology.

---

## Features

### Event Owner

- Sign Up
- Login
- Create Events
- Upload Event Photos
- Manage Event Gallery

### Guest Users

Guests do not need to create an account.

They can:

- Upload a selfie
- Search their photos
- View all matched event images

---

## Face Recognition Pipeline

1. User uploads a selfie.
2. MTCNN detects faces.
3. FaceNet generates embeddings.
4. Embeddings are compared with event photos.
5. Matching images are returned.

---

## Tech Stack

### Backend

- Spring Boot
- Spring Security
- JPA / Hibernate
- MySQL

### ML Service

- FastAPI
- MTCNN
- FaceNet

### Storage

- Google Drive API

---

## Project Structure

```text
EventVision/

├── src/
├── ml-service/
│   ├── app.py
│   ├── face_service.py
│   └── requirements.txt

├── pom.xml

├── README.md

├── .gitignore
```

---

## Setup Instructions

Clone Repository

```bash
git clone https://github.com/Hrishi-18-ctrl/EventVision.git
```

Move into project

```bash
cd EventVision
```

---

### Backend Setup

Create:

```text
application.properties
```

from:

```text
application-example.properties
```

Run backend

```bash
./mvnw spring-boot:run
```

---

### ML Service Setup

Move into ML Service

```bash
cd ml-service
```

Create virtual environment

```bash
python -m venv venv
```

Activate environment

Linux

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run FastAPI

```bash
uvicorn app:app --reload
```

---

### Database Setup

Create database

```sql
CREATE DATABASE eventvision;
```

---

### Google Credentials

Create:

```text
credentials.json
```

from:

```text
credentials-example.json
```

Place it inside:

```text
src/main/resources/
```

---

## Configuration Files

Ignored from GitHub

```text
application.properties
credentials.json
```

Template files provided

```text
application-example.properties
credentials-example.json
```

---

## Future Improvements

- Docker Support
- AWS Deployment
- Email Notifications
- Real-time Processing
- Multi-event Face Search

---

## Author

Hrishikesh Shinde

EventVision – Event Gallery Face Detection System
