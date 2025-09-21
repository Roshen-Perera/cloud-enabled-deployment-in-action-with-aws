# Cloud Enabled Deployment In Action with AWS

This repository contains four projects:

* **course-service** (Spring Boot + MySQL)
* **student-service** (Spring Boot + MongoDB)
* **media-service** (Spring Boot + Local file storage, can be extended to S3/MinIO)
* **frontend-app** (React + TypeScript)

---

## Backend Services

### 1. course-service

* **Entity**: Course(id, name, duration)
* **Endpoints**:

  * `GET /courses`
  * `GET /courses/{id}`
  * `POST /courses`
  * `DELETE /courses/{id}`
* **Default port**: `8081`
* Configure **MySQL** settings

---

### 2. student-service

* **Document**: Student(registrationNumber, fullName, address, contact, email)
* **Endpoints**:

  * `GET /students`
  * `GET /students/{id}`
  * `POST /students`
  * `DELETE /students/{id}`
* **Default port**: `8082`
* Configure **MongoDB** settings

---

### 3. media-service

* **Resource**: files
* **Endpoints**:

  * `POST /files` (multipart/form-data: file)
  * `GET /files` (list)
  * `GET /files/{id}` (fetch)
  * `DELETE /files/{id}` (delete)
* **Default port**: `8083`
* Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`).

---

## Frontend (frontend-app)

* Built with **React + TypeScript + MUI + Axios + Vite**
* Contains 3 sections: **Courses, Students, Media**
* **Scripts**:

  * `npm run dev` → Start Vite dev server
  * `npm run build` → TypeScript build + Vite build
  * `npm run preview` → Preview built app

---

## Build Instructions

* **Backend**: Run

  ```sh
  mvn -q -e -DskipTests package
  ```

  at the repo root to build services.

* **Frontend**: Run

  ```sh
  cd frontend-app
  npm install
  npm run dev
  ```

---

## Author

**Name**: Roshen Perera
**Student ID**: 2301671023

---

## Screen Recording

📺 [Watch the Demo](https://example.com/screen-recording-link)

---
