# capstone Project-SQL
## The Challenge
Airline operations are intricate. A single booking can include multiple passengers, multiple connecting flights, and multiple boarding passes — all tied together with strict rules on seat assignments and flight routes. The task was to design and understand a relational database that could accurately represent this complexity.

### The Journey
Setting the Stage:
Began by understanding the business logic — recognizing that passengers aren’t separate entities but are tied directly to their tickets, with unique ticket numbers serving as the main identifiers.

Mapping the Movements:
Designed a structure where each ticket could involve multiple flight segments (ticket_flights) to accommodate scenarios like round-trips and connecting flights.

Defining Flights:
Each flight (flights) connects two airports — departure and destination — with the same flight number used across different dates, separating operational and schedule data cleanly.

Check-In Complexity:
Introduced boarding passes (boarding_passes), ensuring that a flight-seat combination remains unique, preventing any double-booking of seats.

Aircraft Realities:
Integrated aircraft models (aircrafts) and seat layouts (seats) to reflect real-world cabin configurations. Each aircraft model assumes a single standard configuration.

Schema Integrity:
Although full database-level constraints (like seat existence verification) were not enforced directly in the schema, these were acknowledged as checks to be handled via application logic or triggers — a nod to the complexities faced in production systems.

### The Learning
This project offered a deep dive into practical database design principles:
How to model many-to-many relationships.
The challenges of ensuring data consistency in dynamic systems.
Balancing between database-level constraints and application-level validations.
