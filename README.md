# CyDormSystem (`CDS`)

Software architecture project for **NSWI130 — Software System Architectures**.
CyDormSystem is a web application for managing student dormitories: facility bookings (laundry, study rooms), rent invoicing and payments, resident registration, complaints, and maintenance/housekeeping workflows.

[Shared Google Docs](https://docs.google.com/document/d/1CI1po3fTwbwwlXHs3s7oxI6n99tEUuBOWN9WazaMMmI/edit?usp=sharing)

## Repository Structure

```text
CyDormSystem/
├── 01-requirements/
│   └── features-and-responsibilities.md
├── 02-decomposition/
│   ├── architecture-draft.md
│   └── architecture-decomposition.pdf
├── 03-c4-model/
│   ├── dynamic-diagram/
│   │   ├── student-registration-dynamic-diagram.png
│   │   └── study-room-gym-booking-dynamic-diagram.drawio.png
│   ├── C4-l3-UI.drawio.png
│   ├── c4-l1-system.drawio.png
│   ├── c4-l2-container.drawio.png
│   ├── c4-l3-api-application.drawio.png
│   ├── c4-l3-background-worker.drawio.png
│   ├── c4-deployment-dev.drawio.png
│   └── c4-deployment-production.drawio.png
├── 04-qualities-and-decisions/
│   └── adr/
│       └── README.md
└── 05-peer-review/
```

## 01 — Requirements (`01-requirements/`)

- [Features and Responsibilities](./01-requirements/features-and-responsibilities.md)

## 02 — Architecture Decomposition (`02-decomposition/`)

- [Architecture Draft](./02-decomposition/architecture-draft.md)
- [Architecture Decomposition (PDF)](./02-decomposition/architecture-decomposition.pdf)

## 03 — C4 Model (`03-c4-model/`)

- [C4 Level 1 — System Context](./03-c4-model/c4-l1-system.drawio.png)
- [C4 Level 2 — Container](./03-c4-model/c4-l2-container.drawio.png)
- [C4 Level 3 — Component: API Application](./03-c4-model/c4-l3-api-application.drawio.png)
- [C4 Level 3 — Component: Background Worker](./03-c4-model/c4-l3-background-worker.drawio.png)
- [C4 Level 3 — Component: UI](./03-c4-model/C4-l3-UI.drawio.png)
- [C4 Dynamic — Student Registration](./03-c4-model/dynamic-diagram/student-registration-dynamic-diagram.png)
- [C4 Dynamic — Study Room and Gym Booking](./03-c4-model/dynamic-diagram/study-room-gym-booking-dynamic-diagram.drawio.png)
- [C4 Deployment — Development / Testing](./03-c4-model/c4-deployment-dev.drawio.png)
- [C4 Deployment — Production](./03-c4-model/c4-deployment-production.drawio.png)

## 04 — Qualities & Decisions (`04-qualities-and-decisions/`)

- [Architecture Decision Records (ADR)](./04-qualities-and-decisions/adr/README.md)

## 05 — Peer Review (`05-peer-review/`)

- *Partner team architecture review (to be added)*

https://www.canva.com/design/DAHbxbVViwA/yAezLVOD2kuNXQJ8R6oMpw/edit

https://docs.google.com/document/d/1CI1po3fTwbwwlXHs3s7oxI6n99tEUuBOWN9WazaMMmI/edit?tab=t.0
