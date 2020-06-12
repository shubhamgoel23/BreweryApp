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


# beer service implementation
- createBeer, getBeerById, UpdateBeerById, getBeerByUpcCode, listBeers
schema- beerName, beerStyle, upc, quantityOnHand, price



# Technology:
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

# API Versioning
api/v1/
versioning helps to evolve api without breaking existing api customers
Semantic Versioning 2.0.0
https://semver.org/
non breaking changes: new optional paras, new response fields, new service, bug fixes(behavior chnage, not change to api

Breaking chnages: new required params, removal of existing param, removal of response value, parameter name change or type, deprication of service

https://github.com/lyndseypadget/semflow

# to close issue on github
commit <Closes #1>

# Why you should care about copyright
https://jeroenmols.com/blog/2016/08/03/copyright/
https://choosealicense.com/
use eclipse copyright generator plugin to put copyright on all source files

# project lombok
https://www.baeldung.com/intro-to-project-lombok

# mapstruct
https://www.baeldung.com/mapstruct



# Auto increment keys vs. UUID
https://medium.com/@Mareks_082/auto-increment-keys-vs-uuid-a74d81f7476a
https://www.baeldung.com/hibernate-identifiers
https://www.baeldung.com/java-serial-version-uid

# @version hibernate
https://stackoverflow.com/questions/13374604/when-to-use-version-and-audited-in-hibernate#:~:text=%40Version%20is%20used%20to%20implement,same%20time%20with%20a%20conflict.&text=Before%20committing%2C%20each%20transaction%20verifies,transaction%20has%20modified%20its%20data.
https://dzone.com/articles/version-based-optimistic

# Hibernate Envers : audit
https://www.baeldung.com/database-auditing-jpa
https://vladmihalcea.com/the-best-way-to-implement-an-audit-log-using-hibernate-envers/
https://docs.jboss.org/envers/docs/

# hibernate envers vs javers
https://javers.org/blog/2017/12/javers-vs-envers-comparision.html#:~:text=There%20are%20two%20big%20differences,only%20with%20traditional%20SQL%20databases.&text=On%20the%20contrary%2C%20JaVers%20can,any%20kind%20of%20persistence%20framework.
# JPA Auditing
https://docs.spring.io/spring-data/jpa/docs/1.7.0.DATAJPA-580-SNAPSHOT/reference/html/auditing.html
http://progressivecoder.com/spring-boot-jpa-auditing-example-with-auditoraware-interface/
https://dzone.com/articles/spring-data-jpa-auditing-automatically-the-good-stuff

# identifying/solving hibernate n+1 problems
https://medium.com/sipios/eliminate-spring-hibernate-n-plus-1-queries-f0bcf6a83de2
https://medium.com/@mansoor_ali/hibernate-n-1-queries-problem-8a926b69f618
https://medium.com/@gdprao/fixing-hibernate-n-1-problem-in-spring-boot-application-a99c38c5177d

# data encryption jpa
https://medium.com/faun/spring-boot-jpa-data-encryption-a8e7cacfa8e8
http://www.jasypt.org/hibernate.html#:~:text=For%20encryption%20at%20Hibernate%2C%20jasypt,encryptors%20created%20by%20the%20user.
https://www.baeldung.com/spring-boot-jasypt


# JUNIT
spring security test jar
testing controllers with authenticated active
createSecuritycontext mock authentication and security context
https://www.javacodegeeks.com/2017/05/mocking-spring-security-context-unit-testing.html
https://stackoverflow.com/questions/360520/unit-testing-with-spring-security
@Test
@WithMockUser(username = "admin", authorities = { "ADMIN", "USER" })

https://docs.spring.io/spring-security/site/docs/4.2.x/reference/html/test-method.html
https://docs.spring.io/spring-security/site/docs/4.0.x/reference/htmlsingle/#test-method-withmockuser
@WithMockUser, @WithUserDetails and @WithSecurityContext

Spring Security for Spring Boot Integration Tests
https://www.baeldung.com/spring-security-integration-tests


# Generating Barcodes and QR Codes in Java
https://www.baeldung.com/java-generating-barcodes-qr-codes

# using offsetdatetime to store dates in db
https://www.baeldung.com/java-zoneddatetime-offsetdatetime

# timezone problems in application
https://www.baeldung.com/mysql-jdbc-timezone-spring-boot

# Implementing spring security based or roles, permision, 
https://medium.com/sfl-newsroom/spring-security-expression-based-access-control-56411a60ab3b

# Authorization Models
https://dinolai.com/notes/others/authorization-models-acl-dac-mac-rbac-abac.html
https://medium.com/@mikesparr/security-models-authentication-and-authorization-explained-7c227f228723
https://heap.io/blog/engineering/structure-permissions-saas-app

https://dzone.com/articles/acl-rbac-abac-pbac-radac-and-a-dash-of-cbac


# jackson
https://www.baeldung.com/jackson-ignore-properties-on-serialization
https://www.baeldung.com/jackson-ignore-null-fields
https://www.baeldung.com/jackson-deserialize-json-unknown-properties

# trim leading/trailing whitespace
https://stackoverflow.com/questions/6852213/can-jackson-be-configured-to-trim-leading-trailing-whitespace-from-all-string-pr


# flyway
https://www.baeldung.com/database-migrations-with-flyway

# chaosmonkey
https://www.baeldung.com/spring-boot-chaos-monkey
https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116

# keyclock
https://www.baeldung.com/spring-boot-keycloak

# Feign Client vs RestTemplate
https://www.baeldung.com/intro-to-feign
https://www.baeldung.com/spring-cloud-openfeign
https://medium.com/@darguelles.rojas91/amazing-rest-clients-with-mr-feign-6195d5499a38
https://stackoverflow.com/questions/46884362/what-are-the-advantages-and-disadvantages-of-using-feign-over-resttemplate

# mocking resttemplate
https://www.baeldung.com/spring-mock-rest-template

# mocking feign client
https://stackoverflow.com/questions/53690959/feign-client-mocking-in-in-junit-implementation
https://stackoverflow.com/questions/39465990/how-to-write-integration-tests-with-spring-cloud-netflix-and-feign

# feign client exception handling
https://www.appsdeveloperblog.com/feign-error-handling-with-errordecoder/

# rest template exception handling
https://www.baeldung.com/spring-rest-template-error-handling

# wiremock
https://www.baeldung.com/introduction-to-wiremock


# netflix
https://netflixtechblog.com/how-netflix-microservices-tackle-dataset-pub-sub-4a068adcc9a

