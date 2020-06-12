# BreweryApp
Beer BeerInventory BeerOrders Customer

TastingRoom: Brewery will consume beerInventory for tastingRoom orders
Demand triggers inventory reduction
inventory reduction triggers brewing of beer
brewing will create inventory

# BeerService
manage beers
manage brewing
list beers
validate orders

# BeerOrderService'
manager beer orders
manage lifecycle of order -(from order placement to order shipment)
manage customers
listen order events

# BeerInventoryService
manage beer inventory
takes in inventory from brewing opeartions
provides inventory for orders


Technology:
springBoot, springDataJpa, springMvc, projectLombok, Mapstruct, springScheduledTasks, springEvents,
redis, flyway,feign client, spring security sso, oauth, auditConfiguration, swagger, databaseSharding,
dataEncyption, databaseViews, database Triggers, lazyloading(n+1), GridFsService, HATEOS,json custom deserilize,
producing json and xml both, using forward headers, cors configuration, logging, junit, sonar, jacoco, maven, thymleaf,
jms, spring sagas,spring cloud, circleci/travis, REDOC, hibernate emptyInterceptors, 

DDD: domain driven design
Bounded Context:
example:
Inventory
OrderAllocation
Shipping/Manifest system
Labor Tracking


