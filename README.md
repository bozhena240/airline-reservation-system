# A comprehensive airline management database system that handles flight scheduling, aircraft inventory, passenger reservations, and operational logistics for an airline company.

## Core Tables (9 Entities)
AIRPORT - Stores airport information (codes, names, cities, states)

AIRPLANE_TYPE - Aircraft specifications (models, capacity, manufacturers)

AIRPLANE - Physical aircraft inventory

FLIGHT - Flight definitions and airline information

FLIGHT_LEG - Non-stop flight segments

LEG_INSTANCE - Actual flight occurrences on specific dates

FARE - Pricing rules and fare classes

SEAT - Passenger seat assignments

CAN_LAND - Airport-aircraft compatibility matrix

## Key Relationships
CAN_LAND: Ensures aircraft can safely land at airports

INSTANCE_OF: Links flight legs to specific dates

ASSIGNED: Assigns physical aircraft to flight instances

RESERVATION: Complete booking records (passenger + seat + flight)

## Business Rules & Constraints
5 Critical Business Rules Implemented:
Flight Scheduling Integrity: Departure and arrival airports must be distinct

Reservation Capacity: Prevents overbooking and double bookings

Seat Availability: Available seats must match actual bookings

Aircraft Landing Compatibility: Ensures aircraft can land at assigned airports

Positive Fare Values: All fares must be non-negative

