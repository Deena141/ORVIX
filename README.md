🎯 Problem Statement

In colleges and organizations, multiple events may be planned at the same time. Organizers need to coordinate venues, dates, timings, and participants. When two events require the same venue or overlap in timing, scheduling conflicts can occur.

A centralized system is needed to create and manage events, allocate venues, manage participants, detect scheduling conflicts, and suggest suitable alternatives.


## Technical Stack

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **Analytics:** Chart.js
- **Tools:** VS Code, GitHub
ARCHITECTURE
                    ┌──────────────────────────┐
                    │     ORGANIZER / ADMIN    │
                    └────────────┬─────────────┘
                                 ↓
                    ┌──────────────────────────┐
                    │      WEB INTERFACE       │
                    │    Event Management      │
                    └────────────┬─────────────┘
                                 ↓
          ┌─────────────────────────────────────────┐
          │        EVENT MANAGEMENT MODULE          │
          │                                         │
          │  • Event Creation                       │
          │  • Participant Management & Registration│
          │  • Venue Management                     │
          │  • Schedule Management                  │
          └────────────────────┬────────────────────┘
                               ↓
      ╔══════════════════════════════════════════════════╗
      ║             SMART SCHEDULING ENGINE              ║
      ║                                                  ║
      ║     Event Details: Date + Time + Venue           ║
      ║                      ↓                           ║
      ║            Venue Availability Check              ║
      ║                      ↓                           ║
      ║             Time Availability Check              ║
      ║                      ↓                           ║
      ║              Schedule Validation                 ║
      ║                      ↓                           ║
      ║               Conflict Detection                 ║
      ║                      ↓                           ║
      ║                 ┌───────────┐                    ║
      ║                 │ CONFLICT? │                    ║
      ║                 └─────┬─────┘                    ║
      ║                  YES  │  NO                      ║
      ║                   ↓   │   ↓                      ║
      ║     Find Available    │   Confirm & Save         ║
      ║     Venues & Time     │   Schedule               ║
      ║     Slots             │                          ║
      ║          ↓            │                          ║
      ║     Check Capacity    │                          ║
      ║     & Availability    │                          ║
      ║          ↓            │                          ║
      ║   Suggest Suitable    │                          ║
      ║   Alternatives        │                          ║
      ║          ↓            │                          ║
      ║   Organizer Selects   │                          ║
      ║          ↓            │                          ║
      ║    Confirm Schedule  ─┘                         ║
      ╚═══════════════════════╤══════════════════════════╝
                              ↓
                    ┌─────────────────────┐
                    │      DATABASE       │
                    │                     │
                    │  • Events           │
                    │  • Venues           │
                    │  • Participants     │
                    │  • Schedules        │
                    └──────────┬──────────┘
                               ↓
              ┌────────────────────────────────┐
              │       ORGANIZER DASHBOARD      │
              │                                │
              │  • Event Status                │
              │  • Schedules                   │
              │  • Participants                │
              │  • Event Analytics             │
              └────────────────────────────────┘
Team Name    : ORVIX
Team members : 1.Naveen D.A
               2.Deena Dayalan R
               3.Subash R
College Name  :VSB college of engineering technical campus,coimbatore 
