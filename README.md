# Dental Database Application

This project is a dental clinic management system that includes functions and stored procedures to manage patient visits, treatments, and dentists. The application uses PostgreSQL for database operations and Python to interface with the database.

## Features

1. **Patient Management**
   - Manage patient records, including names, addresses, and payment status.

2. **Visit Management**
   - Keep track of visits between patients and dentists, including visit dates, durations, and treatments.

3. **Treatment Tracking**
   - Record treatments done during visits and track payment status.

4. **Dentist Information**
   - Store dentist information like name, address, and dental school.

## Main Functions

### 1. `cancelSomeVisitsFunction.pgsql`
A PostgreSQL function that cancels future visits for patients who have unpaid treatments. It will cancel up to a specified number of future visits.

**Parameters**:  
- `maxVisitCancellations (INTEGER)`: The maximum number of visits to cancel.

**Returns**:  
- The number of visits cancelled.

### 2. `fireSomePlayersFunction.pgsql`
A PostgreSQL function to remove players from teams based on certain criteria (e.g., low ratings, high playtime).

**Parameters**:  
- `maxFired (INTEGER)`: The maximum number of players to be fired.

**Returns**:  
- The number of players fired.

### 3. Python Application (`rundentalapp.py`)
A Python script that connects to the PostgreSQL database and tests various functionalities.

#### Functions in Python:
- **`countNumberOfPatients(myConn, dentistID)`**: Counts the number of unique patients for a given dentist.
- **`emphasizeToothSide(myConn, toothSide)`**: Updates tooth names to emphasize whether they are on the left or right side.
- **`cancelSomeVisits(myConn, maxVisitCancellations)`**: Calls the PostgreSQL function to cancel future visits.

## Database Schema

- **Patients**: Stores patient information.
- **Dentists**: Stores dentist details.
- **Visits**: Records visits between patients and dentists.
- **DentalTreatments**: Defines dental treatments available.
- **TreatmentsDuringVisits**: Tracks treatments performed during visits.
