# Community Management Website (NoAIcode)

## General System Design

### UI Flow

    Login
        V
    Main frame: Navbar + (Content)

        Dashboard

        Players Management (Players list)
            V
            (Floating) Player Detail
            (Floating) Add Player

        Events Management (Events list)     - Events list mode (Default)
            V                                   
            (Floating) Event Detail
            (Floating) Create Event
            (Floating) Generate Fee Entry 

        Fees Management                     - Overview Grid Mode (All players + events + fees) (Default)
            V                               - Filtered (Name, Team, Event) + Sort
            (Floating) Print
### Use cases and Functionality

    Login
        Login
        Logout

    Dashboard
        R players, events, fees
        Create Event
        Print

    Players Management
        CRUD player
        R players, events, fees
        Print - By a Player

    Events Management
        CRUD event
        Generate fee entry (1. Manual + 2. Auto text -> entry)
        Face Recognition Attendance (Add-ons)

    Fees Management
        CRUD fee 
        R players, events, fees
        Filter
        Sort
        Print - Whole, Whole(Seperated files by Team), By a Team, By a Player.
        Agentic Payment Auditor (Add-ons)

## Project Timeline
    Phase 1: The Core Platform

    Backend (Foundations) (12 days + 2 days for backup)
        * Data Structure

            Data definitions
                * Basic:
                Player
                Event
                Attendance
                PaymentEntry
                * Secondary:
                ManualAdjustment
                * Enums: FeeType, PaymentStatus, EntryType
                    
            Database
                schema creation
                seeding
                converter creation

            Functions / Core Features
                Basic: Player, Event, Attendance, PaymentEntry
                Secondary: Print, Generate fee entry (Manual), Generate fee entry (Auto), Agentic Payment Auditor, Face Recognition Attendance (Nice to have), Search, Filter and Sort.

    Frontend (7 days development + 3 days for back up)
        * Static Frontend

        Login
        Dashboard
        Players Management (Players list)
            (Floating) Player Detail
            (Floating) Add Player
        Events Management (Events list)             
            (Floating) Event Detail
            (Floating) Create Event
            (Floating) Generate Fee Entry 
        Fees Management
            (Floating) Print
        If possible - Users side UI

        * Dynamic Integration

        Login
        Dashboard
        Players Management (Players list)
        Events Management (Events list)

    Testing (3 days)

        * Integration Test
        * End to End
        * Edge Cases

    Deploying (2 days)

    Phase 2: The "Add-Ons" Update (Post-Launch) (7 days)