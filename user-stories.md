# User Stories

## story #1: Booking a meeting room
As a Employee
I want to book a conference for a specific date and time
so that I can hold meetings without scheduling conflicts

### Acceptance Criteria
- [] Given available rooms, When I select a valid date and time, Then available rooms are displayed

- []Given I  enter an invalid or empty date/time , When I try to book, The I see a message: :"Please enter or select a valid date and time"

- Given i try to book the room that  is already booked, when I try to confirm, Then I see an error message: "Room not available for this time" 

### Story Points
- 3
### Priority
- High
### Dependencies
- None
### Technical Notes
- Real-time availability validation required
- Simple booking form
### Design Notes
- Calender and time picker inputs

## story #2  : Set up recurring Meetings
As a Employee
I want to book the same room for many days
So that I don't book again and again
### Acceptance Criteria
- [] Given i booked a room, when I choose recurring option, Then I can set how often
- [] Given dates are okay, when I confirm, Then all bookings are saved
- [] Given one or more conflicting dates, When I save recurrence, Then I see a message: "One or more recurring dates are unavailable."

### Story Points
- 5
### Priority
- Medium
### Dependencies
- Story 1
### Technical Notes
- Calender repeat option
### Design Notes
- Clear repeat settings(daily/weekly)

## story #3: Filter rooms by Size or capacity
As a Employee
I want to filter rooms by size
so that I can select a room that have enough space to fit my team

### Acceptance Criteria
- [] Given I open room list, When I choose size filter, Then only matching rooms shows
- [] Given no room matches, When I filter, Then i see a message: "No room match your filter"
- [] Given I enter invalid size, when I apply filter, Then I see an error message: "Please enter a valid size. "

### Story Points
- 3
### Priority
- High
### Dependencies
- Story 1
### Technical Notes
- Simple filter logic
### Design Notes
- Dropdown or slider for size

## story #4  : Cancel a booking
As a Employee
I want to cancel my booking
So that others can use the room

### Acceptance Criteria
- [] Given my booking, When I cancel it, Then the booking is removed
- [] Given a cancelled booking, When others search, Then the room is available
- [] Given time passed, When I try to cancel, Then I see an erro message: "Cannot cancel after deadline. "


### Story Points
- 2
### Priority
- High
### Dependencies
- Story 1
### Technical Notes
- Update booking status
### Design Notes
- Clear "Cancel booking" button

## story #5  : Select required room equipment
As a Employee
I want to be able to request for equipment
So that I have what I need for my meetings

### Acceptance Criteria
- [] Given I book a room, when I choose equipment, Then I choose equipment, Then it's saved
- [] Given Items not available,When I choose it, Then I see an error message: "Equipment not available. "
- [] Given a booking, When confirmed, Then equipment requirements are saved


### Story Points
- 3
### Priority
- Medium
### Dependencies
- Story 1
### Technical Notes
- Equipment linked to booking
### Design Notes
- Simple checkbox list for equipment

## story #6  : View admin dashboard
As an Admin
I want to view all bookings in a dashboard
So that I can monitor system usage

### Acceptance Criteria
- [] Given admin login, When I access the dashboard, Then all bookings are displayed
- [] Given filters, When applied, Then the dashboard updates
- [] Given no data matches filters, When applied, Then I see an message: "No bookings found for the selected criteria."


### Story Points
- 8
### Priority
- High
### Dependencies
- none
### Technical Notes
- Admin-only access control required
### Design Notes
- Table view with filters and sorting

## story #7  : Schedule room maintenance
As a Facilities Manager
I want to schedule room maintenance
So that rooms cannot be booked during repairs

### Acceptance Criteria
 - [] Given valid maintenance dates, When saved, Then the room is blocked

 - [] Given maintenance overlaps a booking, When saved, Then I see an error message: "Maintenance dates conflict with an existing booking."

 - [] Given an invalid date range, When saved, Then I see an error message: "Invalid maintenance date range."


### Story Points
- 5
### Priority
- Medium
### Dependencies
- None
### Technical Notes
- Repair flag in system
### Design Notes
- Simple date picker

## story #8  : Assist Visitor bookings
As a Receptionist
I want to create bookings for visitors
So that guests can attend meetings smoothly

### Acceptance Criteria
- [] Given complete visitor details, When I save the booking, Then it is created successfully
- [] Given missing visitor details, When I save, Then I see a error message: "Please fill all required fields."
-[] Given an unavailable room, When I save, Then I see an message "Selected room is unavailable."


### Story Points
- 2
### Priority
- Medium
### Dependencies
- Story 1
### Technical Notes
- Receptionist access
### Design Notes
- Simple form

## story #9  : Resolve booking conflicts
As an Admin
I want to resolve booking conflicts
So that scheduling issues are corrected

### Acceptance Criteria
- [] Given two bookings clash, When I check dashboard, Then confict is shown
- [] Given a detected conflict, When I apply a resolution, Then bookings are updated
- [] Given a resolved conflict, When accessed again, Then I see an message: "Booking conflict no longer exists."


### Story Points
- 8
### Priority
- High
### Dependencies
- Story 1
### Technical Notes
- Conflict check logic
### Design Notes
- Clear conflicts alerts

## story #10  : Generate Usage Report
As an Admin
I want to generate room usage reports
So that management can analyze room usage

### Acceptance Criteria
- [] Given a valid date range, When I generate a report, Then usage data is displayed
- [] Given no data exists, When generating the report, Then I see an message: "No data available for the selected date range."
- [] Given an unsupported export type, When exporting, Then I see an error message: "Export format not supported."


### Story Points
- 8
### Priority
- Medium
### Dependencies
- Story 6
### Technical Notes
- Data export
### Design Notes
- Export options(PDF/CSV)