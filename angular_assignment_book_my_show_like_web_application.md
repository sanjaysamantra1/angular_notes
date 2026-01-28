# Angular Assignment: BookMyShow-like Web Application

## 1. REQUIREMENT DOCUMENT

### 1.1 Problem Statement
Design and build a BookMyShow-like web application that allows users to browse events (movies, shows, plays), view details, select seats, and book tickets online. The application is intended for learning, assessment, and portfolio demonstration purposes, focusing on real-world Angular architecture and best practices.

The goal is **not** to replicate BookMyShow fully, but to implement a **simplified yet realistic ticket booking platform**.

---

### 1.2 Target Users
- **End Users (Customers)**: Users who browse events and book tickets
- **Admin Users**: Users who manage movies, events, venues, shows, and pricing
- **Evaluators / Interviewers**: Reviewing architecture, scalability, and Angular best practices

---

### 1.3 Assumptions and Constraints
**Assumptions**
- Backend APIs are mocked or simulated (JSON server / static APIs)
- Payment gateway is simulated (no real transactions)
- Authentication uses dummy credentials or mock JWT
- Single-country and single-currency support

**Constraints**
- Angular 20+ must be used
- RxJS must be used for async data handling
- Lazy loading must be implemented
- No server-side rendering (SSR) required
- No mobile app; web application only

---

### 1.4 Functional Requirements

**User Capabilities**
- User registration and login
- Browse movies/events by category and city
- View event details (description, cast, duration, rating)
- View available shows and timings
- Select seats and number of tickets
- Book tickets and view booking confirmation
- View booking history

**Admin Capabilities**
- Login as admin
- Create, update, delete movies/events
- Manage venues, screens, and seat layouts
- Create and schedule shows
- Set pricing rules

---

### 1.5 Non-Functional Requirements
- Modular and scalable Angular architecture
- Clean separation of concerns
- Responsive UI
- Maintainable folder structure
- Strong typing and RxJS best practices
- Route-level access control
- Error handling and loading states

---

### 1.6 User Flows (High Level)

**User Flow – Booking a Ticket**
1. User logs in
2. Selects city
3. Browses movies/events
4. Selects a movie
5. Chooses show time
6. Selects seats
7. Proceeds to payment
8. Views booking confirmation

**Admin Flow – Managing Shows**
1. Admin logs in
2. Creates/updates a movie
3. Assigns venue and show timings
4. Sets seat pricing

---

## 2. DETAILED LIST OF FEATURES

### 2.1 User-Facing Features
- User authentication (login/register/logout)
- City-based event browsing
- Movie and event listing
- Event detail page
- Show timing selection
- Seat selection UI
- Booking confirmation page
- Booking history

---

### 2.2 Admin Features
- Admin dashboard
- Movie/event management
- Venue and screen management
- Seat layout configuration
- Show scheduling
- Price configuration

---

### 2.3 Payment and Booking Features
- Ticket price calculation
- Convenience fee calculation
- Mock payment processing
- Booking confirmation
- Ticket summary generation

---

### 2.4 Notifications and Communication
- Booking success message
- Payment failure message
- Session timeout handling
- Optional email/SMS simulation (UI only)

---

### 2.5 Security and Access Control
- Role-based access (User vs Admin)
- Route guards
- Token-based authentication (mock JWT)
- Secure route segregation

---

## 3. ANGULAR-SPECIFIC TECHNICAL BREAKDOWN

### 3.1 Feature Modules (Lazy Loaded)
- AuthModule
- UserModule
- AdminModule
- MoviesModule
- BookingModule
- PaymentModule
- CoreModule
- SharedModule

---

### 3.2 Components

**Container (Smart) Components**
- MovieListContainer
- MovieDetailContainer
- BookingContainer
- SeatSelectionContainer
- AdminDashboardContainer

**Presentational (Dumb) Components**
- MovieCardComponent
- ShowTimeComponent
- SeatComponent
- BookingSummaryComponent
- Button / Modal components

---

### 3.3 Custom Directives
- RoleBasedAccessDirective
- HighlightSeatDirective
- ClickOutsideDirective

---

### 3.4 Custom Pipes
- DurationPipe
- PriceFormatPipe
- RatingPipe
- FilterByCityPipe

---

### 3.5 Services
- AuthService
- UserService
- MovieService
- BookingService
- PaymentService
- AdminService
- NotificationService

---

### 3.6 Guards
- AuthGuard
- AdminGuard
- BookingGuard

---

### 3.7 Interceptors
- AuthTokenInterceptor
- ErrorHandlingInterceptor
- LoadingInterceptor

---

### 3.8 Shared Module Items
- Reusable UI components
- Common pipes and directives
- Form validators
- Constants and enums

---

## Submission Expectations
- Clean folder structure
- README explaining setup and assumptions
- Screenshots or short demo (optional)
- Focus on architecture over styling

---

**End of Assignment Document**

