# PesaRide Planning

### System Overview
The app is mainly providing the following functionalities:

- Passengers and drivers can set up their profile while using PesaRide App.
- Passengers and drivers can use PesaRide App to update their real-time location.
- Passengers can use PesaRide App to submit their trip request.
- PesaRide platform can match nearby drivers and assign them to each valid trip.
- Drivers can use PesaRide App to pick up passengers, complete order and get earnings on each trip.

To effectively provide functionalities above, we have designed the following microservices below to enable PesaRide hailing System workflow:

- Trip Gateway Service - Core service, match passenger’s demand and driver’s supply
- Map & Route Service - Provide map service including routes, arrival time.
- Driver Location Service - Store and retrieve drive location & availability status
- Trip Service - Store trip information for retrieving purpose
- Passenger Profile Service - Store passengers profile information
- Driver Profile Service - Store driver profile information
- Payment Service - Utility service to handle payment related functions
- Review Service - Utility service to handle review functions
