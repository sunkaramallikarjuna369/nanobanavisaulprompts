# Diagram Layout Prompts for Gemini Nano Bana

```
╔══════════════════════════════════════════════════════════════╗
║              ARCHITECTURE & DIAGRAM LAYOUTS                   ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Prompt 1: System Architecture Diagram

### Prompt
```
Create a system architecture diagram for a microservices-based 
e-commerce platform. Show: API Gateway, User Service, Product 
Service, Order Service, Payment Service, Notification Service,
Message Queue, and Database for each service. Use boxes and arrows.
```

### Expected Visual Output
```
┌─────────────────────────────────────────────────────────────────┐
│                        LOAD BALANCER                             │
└───────────────────────────┬─────────────────────────────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│                       API GATEWAY                                │
│               (Auth, Rate Limit, Routing)                        │
└──┬──────────┬──────────┬──────────┬──────────┬──────────────────┘
   ▼          ▼          ▼          ▼          ▼
┌────────┐┌────────┐┌────────┐┌────────┐┌────────────┐
│ User   ││Product ││ Order  ││Payment ││Notification│
│Service ││Service ││Service ││Service ││ Service    │
└───┬────┘└───┬────┘└───┬────┘└───┬────┘└─────┬──────┘
    ▼         ▼         ▼         ▼           ▼
┌────────┐┌────────┐┌────────┐┌────────┐  ┌───────┐
│UserDB  ││ProdDB  ││OrderDB ││PayDB   │  │ Email │
│(Postgres)│(Mongo)││(Postgres)│(Postgres)│ │ SMS  │
└────────┘└────────┘└───┬────┘└────────┘  └───────┘
                        │
              ┌─────────▼─────────┐
              │   MESSAGE QUEUE   │
              │    (RabbitMQ)     │
              └───────────────────┘
```

---

## Prompt 2: Entity Relationship Diagram

### Prompt
```
Generate an ER diagram for a learning management system with entities:
Student, Course, Instructor, Enrollment, Assignment, Submission, Grade.
Show relationships with cardinality (1:N, M:N).
```

### Expected Visual Output
```
┌──────────────┐     1:N     ┌──────────────┐
│  INSTRUCTOR  │────────────>│    COURSE    │
│──────────────│             │──────────────│
│ instructor_id│             │ course_id    │
│ name         │             │ title        │
│ department   │             │ credits      │
└──────────────┘             └──────┬───────┘
                                    │ 1:N
                                    ▼
┌──────────────┐    M:N     ┌──────────────┐
│   STUDENT    │<──────────>│  ENROLLMENT  │
│──────────────│            │──────────────│
│ student_id   │            │ enrollment_id│
│ name         │            │ grade        │
│ email        │            │ semester     │
└──────┬───────┘            └──────────────┘
       │ 1:N
       ▼
┌──────────────┐     N:1    ┌──────────────┐
│  SUBMISSION  │────────────│  ASSIGNMENT  │
│──────────────│            │──────────────│
│ submission_id│            │ assignment_id│
│ file_url     │            │ title        │
│ submitted_at │            │ due_date     │
└──────────────┘            └──────────────┘
```

---

## Image Examples

| Prompt | Expected Image Type | Description |
|--------|-------------------|-------------|
| Architecture diagram | Cloud architecture | Color-coded service boxes with directional arrows showing data flow |
| ER diagram | Database schema | Tables with primary/foreign keys connected by relationship lines |
