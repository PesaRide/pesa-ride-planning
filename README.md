# PesaRide Planning

## Introduction
This repo is designed to be a reference of the PesaRide hailing platform as it describes the architecture and requirements, assumptions, and the motivations behind the chosen design. Both high-level and low-level designs are included in this repo.

The challenge for the PesaRide platfrom as a whole is to satisfy the dynamic demand from passengers side and the dynamic supply from drivers side. This repo design specifications provide the guidelines to accomplish this challenge, and make the entire platfrom work in a cost effective and time efficient manner.

## Purpose
At its core, the PesaRide app functions as a matching engine that connects passenger ride requests with available drivers. Designed to serve an urban area of 1.7 million residents, the platform enables passengers to request rides using their real-time location. PesaRide then pairs them with nearby drivers within a specified radius. Once a match is confirmed, the driver picks up the passenger and navigates to the requested destination.

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
