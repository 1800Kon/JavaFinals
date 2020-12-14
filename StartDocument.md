# JavaFinals
## Project definition
This project will consist of an airport managing system. It must be able to do the following:
* Book a flight
* Check profit for a flight (Fuel price / People in the flight / Fuel consumption)
* Show all passengers in each class
* Show all flights from the last 2 weeks

## Assignment:
The assignment is to develop software for an Airport for a private lottery winner. 
The application should print the profits per flight (People in the flight * ticket prices) - ((Fuel price/km)*distance)). 
Through the system it should be possible to book flights via a ticket and attend it.
Lastly the software should keep a flight history of all flights, and a list of names with passengers
and their flight details.

## Stuff for interview
Abstract (Person), subclass from asbtract, Interface (Ticket), 5 classes, try-catch (First class with economy ticket), collections.

## Classes
* Airport
* Airline
* Flights
* Plane
* Person
  * Passenger
  * Pilot
  * Stewardess
* Baggage
* Ticket
  * First class ticket
  * Economy class ticket

## Properties
* Airport
  * Name
  * Location
  * Airlines
  
* Airlines
  * Planes
  * Employees
  * Flights List

* Flights
  * Date and time of flight

## Inputs (Follows Case / Type / Conditions format)
* Airport name / String / X
* Airport location / String / X
* Airline name / String / X
* Flight number / String / Must not be used by another flight
* Departure date / DateTime / Must be in the future
* Flight distance / Double / Can't be negative
* Plane brand / String / X
* Plane model / String / X
* Plane capacity / String / X
* Plane fuel consumption / double / Can't be negative
* Number of first class seats / int / X
* Number of economy class seats / int / X
* Person name / String / X
* Person date of birth / Date / X

## Outputs (Follows Case / Type / Conditions format)
* getAllFlights() / Arraylist of Flights / X
* getProfits() / double / X
* getExpenses() / double / X
* getAllFlightHistory() / Arraylist of Flights / X
* getFlightHistory() / Arraylist of Flights / X
* findCrew() / Arraylist of Employees / X
* getFlightCosts() / Double / X
* checkTicketAvailability() / Boolean / X
* calculateCosts() / Double / X

## UML
![UML](https://i.imgur.com/RpQ1SiV.png)
