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

## 