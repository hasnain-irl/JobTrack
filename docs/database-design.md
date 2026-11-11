
# JobTrack — Database Design

## 1. Overview

JobTrack will use PostgreSQL as its relational database.
SQLAlchemy will be used for database operations and ORM.

## 2. Database Entities

### User

Stores registered user information.

| Field | Type | Description |
|---|---|---|
| id | Integer | Primary key |
| name | String | User's full name |
| email | String | Unique email address |
| password_hash | String | Hashed password |
| created_at | DateTime | Account creation date |

### JobApplication

Stores job applications submitted by users.

| Field | Type | Description |
|---|---|---|
| id | Integer | Primary key |
| user_id | Integer | Foreign key referencing User |
| company_name | String | Company name |
| job_title | String | Position applied for |
| location | String | Job location |
| job_type | String | Employment type |
| status | String | Application status |
| applied_at | DateTime | Application date |
| job_description | Text | Job description |
| created_at | DateTime | Record creation date |

### Interview

Stores interview information.

| Field | Type | Description |
|---|---|---|
| id | Integer | Primary key |
| application_id | Integer | Foreign key referencing JobApplication |
| scheduled_at | DateTime | Interview date and time |
| interview_type | String | Interview type |
| notes | Text | Interview notes |
| outcome | String | Interview outcome |

### ApplicationNote

Stores notes related to job applications.

| Field | Type | Description |
|---|---|---|
| id | Integer | Primary key |
| application_id | Integer | Foreign key referencing JobApplication |
| content | Text | Note content |
| created_at | DateTime | Note creation date |

## 3. Entity Relationships

- One User can have multiple JobApplications.
- One JobApplication belongs to one User.
- One JobApplication can have multiple Interviews.
- One JobApplication can have multiple ApplicationNotes.

## 4. Relationship Diagram

User (1) → (Many) JobApplication

JobApplication (1) → (Many) Interview

JobApplication (1) → (Many) ApplicationNote

## 5. Database Constraints

- User email must be unique.
- Primary keys uniquely identify records.
- Foreign keys maintain relationships.
- Passwords must be stored as secure hashes.
- Each user's applications must remain private.

## 6. Planned Application Statuses

- Applied
- Screening
- Interview
- Offer
- Rejected
- Withdrawn

Note: This is the initial database design.
The schema may be refined during implementation.
