# Presentation Notes – Exact Script
Conference Room Booking System – API & Contract Overview
Presenter: Onthangaho Magoro
Duration: ~7 minutes

---

## Slide 1 – Title & Context (≈30 seconds)

“Good day everyone. My name is Onthangaho Magoro.
Today I will be presenting the Conference Room Booking System,
with a focus on the API and documentation work that has been done so far.

This project was developed as part of a sprint-based simulation.
The goal is not to show a fully built system, but to show how clear
API contracts, documentation, and collaboration practices support
real-world software development.”

---

## Slide 2 – Agenda (≈30 seconds)

“In this presentation, I will first explain the problem the system
is trying to solve. Then I will walk through the high-level workflow
of the booking process.

After that, I will explain the key technical components we used,
how collaboration was handled using Pull Requests, and how
documentation like Swagger and README supports developers.

I will also highlight common risks we identified and briefly
explain what would be shown in a live demo.”

---

## Slide 3 – Problem / System Context (≈45 seconds)

“The main problem this system addresses is double booking of
conference rooms.

In many organisations, rooms are booked manually or using systems
that do not properly check availability. This leads to conflicts,
wasted time, and frustration for employees.

Our system focuses on preventing double bookings by validating
room availability, capacity, and booking rules before a booking
is confirmed.”

---

## Slide 4 – High-Level Workflow (≈45 seconds)

“At a high level, the workflow is simple.

A user sends a booking request through a client application.
That request goes to the API, where validation checks are applied.

The system checks if the room exists, if it is available at the
requested time, and if there are no conflicts.
If all checks pass, the booking is created.
If not, a clear error message is returned to the user.”

---

## Slide 5 – Key Technical Components (≈60 seconds)

“The main technical component in this project is the OpenAPI,
also known as Swagger documentation.

Swagger defines the API endpoints, request formats, responses,
and validation rules. This acts as the contract between frontend
and backend developers.

Postman was used to test the API behaviour. Because the backend
was not running locally, a Postman mock server was used.
This still allowed realistic testing of requests and responses.

Docker is planned for future use to ensure the system can run
consistently across environments.”

---

## Slide 6 – Pull Requests & Collaboration Flow (≈45 seconds)

“All changes in this project are made using feature branches
and Pull Requests.

Instead of committing directly to the main branch, contributors
create a branch, make focused changes, and submit a Pull Request.

The Pull Request explains why the change was made, what was changed,
and what reviewers should focus on.
This improves communication and reduces mistakes.”

---

## Slide 7 – Documentation & Contracts (≈45 seconds)

“Documentation plays a very important role in this project.

The README file supports onboarding of new developers by explaining
the system context, repository structure, and contribution workflow.

Swagger documentation defines the API contract clearly so that
everyone understands how the system should behave.

This reduces misunderstandings and allows development to move faster.”

---

## Slide 8 – Common Pitfalls or Risks (≈45 seconds)

“Some common risks were identified during this work.

One risk is assuming the API is running locally when it is not,
which causes connection errors during testing.

Another risk is unclear acceptance criteria or validation rules,
which can lead to incomplete or incorrect implementations.

Keeping documentation updated is important to reduce these risks.”

---

## Slide 9 – Demo Overview (≈45 seconds)

“If this were a live demo, I would first open the Swagger UI
to show the available endpoints and request structures.

Next, I would open Postman, import the OpenAPI specification,
and show a GET request returning a successful response.

This demo would prove that the API contract is clear and testable,
even without a fully running backend.”

---

## Slide 10 – Summary & Resources (≈30 seconds)

“To summarise, this project focuses on clear API contracts,
good documentation, and professional collaboration practices.

Swagger acts as the source of truth, Postman validates behaviour,
and Pull Requests support teamwork.

All documentation is available in the repository to support
future development and onboarding.

Thank you.”

