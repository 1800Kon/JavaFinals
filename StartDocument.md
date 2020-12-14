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

#Nouns
- Airport
- Airline
- Plane
- Employee
- Passeneger
- Baggage
- Ticket
- Profit
- Expenses

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
  * Hand luggage
  * Suitcase
* Ticket
  * First class ticket
  * Economy class ticket
  
## Inputs (Follows Case / Type / Conditions format)
* Airport name / String / X
* Airport location / String / X
* Airline name / String / X
* Flight number / String / Must not be used by another flight
* Departure date / DateTime / Must be in the future
* Flight distance / Double / Can't be negative
* Destination / String / X
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
![UML](https://i.imgur.com/2tWzWAY.png)

## Test Data

### Airport
| Name  | Location | Airlines  |
|     :---:      |     :---:      |     :---:      |
| US    | United States     | Delta    |
| RD       | Dominican Republic     | RdAirline, RdAirline2     |
| CoolAirport       | Madrid     | X     |

### Airline
| Name  | Planes | flights  |
|     :---:      |     :---:      |     :---:      |
| Delta    | Boeing747     | Flight1    |
| Nitro       | Airbus312, Boeing 747     | Flight2     |
| Turbo       | Boeing7476     | X     |

### Passenger
| Name  | DOB | Ticket  | bags |
|     :---:      |     :---:      |     :---:      |     :---:      |
| Passenger1     | 08/03/2001     | Ticket1    | 2 valid    |
| Passenger2       | 08/03/2001     | Ticket2     | 1 valid 1 too big     |
| Passenger3       | 08/03/2001     | Ticket1     | none    |

### Baggage
| Name   |  Bag1 | Bag2 |
|     :---:      |     :---:      |     :---:      |
| Passenger1     | 30 x  30 x 35   | 40 x  20 x 35    | 
| Passenger2       | 30 x  30 x 25     | 30 x  30 x 35     | 
| Passenger3       | x     | x     | 

### Flight
 Flight number  | Plane | Date  | Distance | Destination |
|     :---:      |     :---:      |     :---:      |     :---:      |      :---:      |
| Flight1     | Boeing747     | 14/12/20    | 3000    | Peru    |
| Flight2       | Boeing7476     | 14/12/20     | 22222     | Santo Domingo    |
| Flight3       | Airbus312     | 04/12/20     | 1232    | DunnoMan    |

### Ticket
|Ticket name| Type  | Price | Flight  | Passenger | maxBaggageHeight |maxBaggageWidth |maxBaggageLength |
|     :---:      |     :---:      |     :---:      |     :---:      |     :---:      |  :---:      | :---:      | :---:      |
| Ticket1     | First Class     | 100     | Flight1    | Passenger1    | 80    | 45    |35    |
| Ticket2     | Economy Class       | 50     | Flight1     | Passenger2     |60     |30     |25     |
| Ticket3     | Economy Class       | 50     | Flight2     | Passenger3     |60    |30    |25    |

### Plane
|Plane name| Brand  | Model | Capacity  | fuelConsumptionPerKm | Number of first class seats | Number of economy class seats |
|     :---:      |     :---:      |     :---:      |     :---:      |     :---:      |     :---:      |     :---:      |
| Plane 1     | Boeing    | 747     | 1    | 10    | 1    | 0    |
| Plane 2     | Airbus       | 312     | 2     | 20     | 1    | 1    |
| Plane 3     | Boeing       | 7476     | 3     | 30     | 2   | 1    |

## Test Plan
| Method  | Input | Output  |
|     :---:      |     :---:      |     :---:      |
| US.addAirline()    | Delta     | "Delta was added"    |
| Us.addAirline()    | Delta     | "Delta is already inside the airport"    |
| Us.getAllFLights()    | X     | Flight1    |
| Us.getProfits(Assuming a flight cost of 1000 and a 1500 ticket margin)    | X     | 500    |
| passenger1.addBaggage()    | baggage1     | "The baggage was added"    |
| passenger1.purchaseTicket()    | Flight1     | "The ticket was bought"    |
| passenger1.purchaseTicket()    | Flight1     | "You already bought a ticket"    |
| passenger3.purchaseTicket()    | Flight1     | "Flight1 is currently fully booked"    |
| flight1.checkKTicketAvailability()    | X     | False    |
| flight1.getPlaneCost()    |   Flight1   |  30000   |
| flight2.getFLightCost()    | Boeing747     | 666660    |
| Us.getExpenses()    | X     | 30000    |
| Delta.addEmployee()    | mario     | "Mario has been added to Delta"    |
| Delta.addEmployee()  | mario     | "Mario is already in Delta"    |
| Delta.findCrew()    | X     | "There isnt enough crew for a flight"    |
| Delta.cancelFlight()    | X     | "It is announced that the flight is canceled"    |
| Delta.refundTickets()    | X     | "You were refunded the ticket money"    |
| Delta.findCrew(Assuming enough crew)    | X     | Arraylist of employees    |
| Flight1.arriveToDestination()    | X     | "Flight1 has arrived in Peru"   |
| Flight1.getFlightCosts(Assuming a total salary of 5000)    | X     | 35000    |
| Us.getAllFlightHistory()    | X     | Flight1    |
| Us.getAllFlightHistory(Assuming FLight1, Flight2, and Flight3 have been completed)    | X     | Flight1, FLight2, Flight3    |
