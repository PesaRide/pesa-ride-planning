# PesaRide Planning
## Purpose
The ability to match ride demands from passengers and ride supplies from drivers are the essential function of this PesaRide hailing platfrom. PesaRide App is targeting to provide ride hailing service in a 1.7M population urban city. After downloading the app, passengers can submit their ride request by sending their real-time location, and PesaRide App will match the nearby drivers within certain range of distances. With a successful match, the driver can pick up the passengers and start the route to the destination passenger request.

## System Overview
The app is mainly providing the following functionalities:

- Passengers and drivers can set up their profile while using PesaRide App.
- Passengers and drivers can use PesaRide App to update their real-time location.
- Passengers can use PesaRide App to submit their trip request.
- PesaRide platform can match nearby drivers and assign them to each valid trip.
- Drivers can use PesaRide App to pick up passengers, complete order and get earnings on each trip.


## Microservices
To effectively provide functionalities above, we have designed the following microservices below to enable PesaRide hailing System workflow:

- **Trip Gateway Service** - Core service, match passenger’s demand and driver’s supply
- **Map & Route Service** - Provide map service including routes, arrival time.
- **Driver Location Service** - Store and retrieve drive location & availability status
- **Trip Service** - Store trip information for retrieving purpose
- **Passenger Profile Service** - Store passengers profile information
- **Driver Profile Service** - Store driver profile information
- **Payment Service** - Utility service to handle payment related functions
- **Review Service** - Utility service to handle review functions

## Design Consideration

### Assumptions and Dependencies
#### End-user characteristics:

- **Passengers:**
    - Able to request a ride by giving their real-time location
    - Able to complete the ride with valid payment method

- **Drivers:**
    - Able to find a ride order by giving their real-time location
    - Able to pick up the passengers and drive them to the final destination
