# CAD-Theatre
🎬 Project Documentation: ShowTime Manager
🏷️ Project Title
ShowTime Manager – Smart Theatre Booking and Screen Management System

🎯 Target Audience
  Theatre Owners,Cinema Chain Managers

👤 Team Size
1 (Solo Developer)

💰 Budget
₹0 (Zero)

⏳ Timeline
1 Month

🏢 Type
Business to Business (B2B)

✅ Project Overview
ShowTime Manager is a theatre and screen management platform designed for theatre owners to easily manage showtimes, bookings, seat availability, and screens. It allows quick movie updates, seamless ticket booking, and real-time tracking of seat occupancy, aiming to modernize traditional booking operations.

🔧 Core Features
👤 User Management
User Registration
  Allow theatre staff or admin to register.

User Login
  Secure login for authenticated access.

🎥 Theatre & Movie Management
Add Total Seats
  Configure seat count for each screen.

Add Screens
  Manage multiple screens with unique names, capacity, and layout.

Add Movies
  Add movies with poster, title, language, duration, genre, rating, and showtimes.

Assign Movies to Screens
  Schedule specific movies for particular screens at fixed times.

🎟️ Booking System
Book Ticket
  Users (theatre staff or online) can book tickets based on seat availability.

Cancel Ticket
  Cancel reserved tickets and make seats available again.

View Seat Availability (Real-Time)

Visual seat selection (booked, available, reserved


---Model Class--

class User:-
    int id;
    String name;
    long mobileNo;
    String password;
class Theatre 
    int id;
    String name;
    String location;
    String address;
    List<Screen> screens;

  
class Screen {
    int screenNo;
    int totalSeats;
    boolean isAC;
    List<ShowTime> showTimes; // all shows running in this screen
}
class ShowTime {
    int showid;
    Screen screen;
    long startTime;
    List<Ticket> tickets; // booked tickets for this show
}

class Movie {
    int id;
    int screenid;
    int showId;
    String title;
    String language;
    int durationMinutes;
    String genre;
    double rating;
}
class Ticket {
    int ticketNo;
    int screenId;
    ShowTime showTime;
    int seatCount;
    List<String> seatNumbers; // to support specific seat selection
    long bookingTime;
}









