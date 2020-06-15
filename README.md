# BreweryApp
Beer BeerInventory BeerOrders Customer

TastingRoom: Brewery will consume beerInventory for tastingRoom orders <br/>
Demand triggers inventory reduction<br/>
inventory reduction triggers brewing of beer<br/>
brewing will create inventory<br/>

# BeerService
manage beers<br/>
manage brewing<br/>
list beers<br/>
validate orders<br/>

# BeerOrderService'
manager beer orders<br/>
manage lifecycle of order -(from order placement to order shipment)<br/>
manage customers<br/>
listen order events<br/>

# BeerInventoryService
manage beer inventory<br/>
takes in inventory from brewing opeartions<br/>
provides inventory for orders<br/>


# beer service implementation
- createBeer, getBeerById, UpdateBeerById, getBeerByUpcCode, listBeers<br/>
schema- beerName, beerStyle, upc, quantityOnHand, price<br/>



# Technology:
springBoot, springDataJpa, springMvc, projectLombok, Mapstruct, springScheduledTasks, springEvents,<br/>
redis, flyway,feign client, spring security sso, oauth, auditConfiguration, swagger, databaseSharding,<br/>
dataEncyption, databaseViews, database Triggers, lazyloading(n+1), GridFsService, HATEOS,json custom deserilize,<br/>
producing json and xml both, using forward headers, cors configuration, logging, junit, sonar, jacoco, maven, thymleaf,<br/>
jms, spring sagas,spring cloud, circleci/travis, REDOC, hibernate emptyInterceptors, <br/>

DDD: domain driven design<br/>
Bounded Context:<br/>
example:<br/>
Inventory<br/>
OrderAllocation<br/>
Shipping/Manifest system<br/>
Labor Tracking<br/>

# API Versioning
api/v1/<br/>
versioning helps to evolve api without breaking existing api customers<br/>
Semantic Versioning 2.0.0<br/>
https://semver.org/<br/>
non breaking changes: new optional paras, new response fields, new service, bug fixes(behavior chnage, not change to api<br/>

Breaking chnages: new required params, removal of existing param, removal of response value, parameter name change or type, deprication of service<br/>

https://github.com/lyndseypadget/semflow<br/>

# to close issue on github
commit <Closes #1><br/>

# Why you should care about copyright
https://jeroenmols.com/blog/2016/08/03/copyright/<br/>
https://choosealicense.com/<br/>
use eclipse copyright generator plugin to put copyright on all source files<br/>

# project lombok
https://www.baeldung.com/intro-to-project-lombok<br/>

# mapstruct
https://www.baeldung.com/mapstruct<br/>

# flyway
https://martinfowler.com/articles/evodb.html<br/>
https://medium.com/@ruxijitianu/database-version-control-liquibase-versus-flyway-9872d43ee5a4<br/>
https://stackoverflow.com/questions/39044851/flyway-and-liquibase-together<br/>

# dbcp connection pool
https://commons.apache.org/proper/commons-dbcp/<br/>
https://www.baeldung.com/spring-boot-tomcat-connection-pool<br/>
https://www.baeldung.com/hikaricp<br/>


# Auto increment keys vs. UUID
https://medium.com/@Mareks_082/auto-increment-keys-vs-uuid-a74d81f7476a<br/>
https://www.baeldung.com/hibernate-identifiers<br/>
https://www.baeldung.com/java-serial-version-uid<br/>

# @version hibernate
https://stackoverflow.com/questions/13374604/when-to-use-version-and-audited-in-hibernate#:~:text=%40Version%20is%20used%20to%20implement,same%20time%20with%20a%20conflict.&text=Before%20committing%2C%20each%20transaction%20verifies,transaction%20has%20modified%20its%20data.<br/>
https://dzone.com/articles/version-based-optimistic<br/>

# Hibernate Envers : audit
https://www.baeldung.com/database-auditing-jpa<br/>
https://vladmihalcea.com/the-best-way-to-implement-an-audit-log-using-hibernate-envers/<br/>
https://docs.jboss.org/envers/docs/<br/>

# hibernate envers vs javers
https://javers.org/blog/2017/12/javers-vs-envers-comparision.html#:~:text=There%20are%20two%20big%20differences,only%20with%20traditional%20SQL%20databases.&text=On%20the%20contrary%2C%20JaVers%20can,any%20kind%20of%20persistence%20framework.<br/>
# JPA Auditing
https://docs.spring.io/spring-data/jpa/docs/1.7.0.DATAJPA-580-SNAPSHOT/reference/html/auditing.html<br/>
http://progressivecoder.com/spring-boot-jpa-auditing-example-with-auditoraware-interface/<br/>
https://dzone.com/articles/spring-data-jpa-auditing-automatically-the-good-stuff<br/>

# identifying/solving hibernate n+1 problems
https://medium.com/sipios/eliminate-spring-hibernate-n-plus-1-queries-f0bcf6a83de2<br/>
https://medium.com/@mansoor_ali/hibernate-n-1-queries-problem-8a926b69f618<br/>
https://medium.com/@gdprao/fixing-hibernate-n-1-problem-in-spring-boot-application-a99c38c5177d<br/>

# data encryption jpa
https://medium.com/faun/spring-boot-jpa-data-encryption-a8e7cacfa8e8<br/>
http://www.jasypt.org/hibernate.html#:~:text=For%20encryption%20at%20Hibernate%2C%20jasypt,encryptors%20created%20by%20the%20user.<br/>
https://www.baeldung.com/spring-boot-jasypt<br/>


# JUNIT
spring security test jar<br/>
testing controllers with authenticated active<br/>
createSecuritycontext mock authentication and security context<br/>
https://www.javacodegeeks.com/2017/05/mocking-spring-security-context-unit-testing.html<br/>
https://stackoverflow.com/questions/360520/unit-testing-with-spring-security<br/>
@Test<br/>
@WithMockUser(username = "admin", authorities = { "ADMIN", "USER" })<br/>

https://docs.spring.io/spring-security/site/docs/4.2.x/reference/html/test-method.html<br/>
https://docs.spring.io/spring-security/site/docs/4.0.x/reference/htmlsingle/#test-method-withmockuser<br/>
@WithMockUser, @WithUserDetails and @WithSecurityContext<br/>
<br/>
Spring Security for Spring Boot Integration Tests<br/>
https://www.baeldung.com/spring-security-integration-tests<br/>


# Generating Barcodes and QR Codes in Java
https://www.baeldung.com/java-generating-barcodes-qr-codes<br/>

# using offsetdatetime to store dates in db
https://www.baeldung.com/java-zoneddatetime-offsetdatetime<br/>

# timezone problems in application
https://www.baeldung.com/mysql-jdbc-timezone-spring-boot<br/>

# Implementing spring security based or roles, permision, 
https://medium.com/sfl-newsroom/spring-security-expression-based-access-control-56411a60ab3b<br/>

# Authorization Models
https://dinolai.com/notes/others/authorization-models-acl-dac-mac-rbac-abac.html<br/>
https://medium.com/@mikesparr/security-models-authentication-and-authorization-explained-7c227f228723<br/>
https://heap.io/blog/engineering/structure-permissions-saas-app<br/>
<br/>
https://dzone.com/articles/acl-rbac-abac-pbac-radac-and-a-dash-of-cbac<br/>
<br/>

# jackson
https://www.baeldung.com/jackson-ignore-properties-on-serialization<br/>
https://www.baeldung.com/jackson-ignore-null-fields<br/>
https://www.baeldung.com/jackson-deserialize-json-unknown-properties<br/>

# trim leading/trailing whitespace
https://stackoverflow.com/questions/6852213/can-jackson-be-configured-to-trim-leading-trailing-whitespace-from-all-string-pr<br/>
<br/>

# flyway
https://www.baeldung.com/database-migrations-with-flyway<br/>

# chaosmonkey
https://www.baeldung.com/spring-boot-chaos-monkey<br/>
https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116<br/>

# keyclock
https://www.baeldung.com/spring-boot-keycloak<br/>

# Feign Client vs RestTemplate
https://www.baeldung.com/intro-to-feign<br/>
https://www.baeldung.com/spring-cloud-openfeign<br/>
https://medium.com/@darguelles.rojas91/amazing-rest-clients-with-mr-feign-6195d5499a38<br/>
https://stackoverflow.com/questions/46884362/what-are-the-advantages-and-disadvantages-of-using-feign-over-resttemplate<br/>

# mocking resttemplate
https://www.baeldung.com/spring-mock-rest-template<br/>

# mocking feign client
https://stackoverflow.com/questions/53690959/feign-client-mocking-in-in-junit-implementation<br/>
https://stackoverflow.com/questions/39465990/how-to-write-integration-tests-with-spring-cloud-netflix-and-feign<br/>

# feign client exception handling
https://www.appsdeveloperblog.com/feign-error-handling-with-errordecoder/<br/>

# rest template exception handling
https://www.baeldung.com/spring-rest-template-error-handling<br/>

# wiremock
https://www.baeldung.com/introduction-to-wiremock<br/>


# netflix
https://netflixtechblog.com/how-netflix-microservices-tackle-dataset-pub-sub-4a068adcc9a<br/>

# Securing Application
https://developer.okta.com/blog/2018/07/30/10-ways-to-secure-spring-boot<br/>
https://snyk.io/<br/>
https://docs.spring.io/spring-security/site/docs/5.0.x/reference/html/headers.html<br/>
https://securityheaders.com/<br/>
https://owasp.org/<br/>
https://github.com/zaproxy/zaproxy<br/>
https://medium.com/@marianfurdui/generate-a-java-keystore-from-lets-encrypt-for-java-web-spring-or-spring-boot-applications-bf07408158ef <br/>
https://developer.okta.com/blog/2020/03/23/microservice-security-patterns#4-use-access-and-identity-tokens<br/>
https://developer.okta.com/blog/2020/03/27/spring-oidc-logout-options<br/>
https://developer.okta.com/docs/reference/rate-limits/<br/>
https://www.baeldung.com/spring-bucket4j<br/>
https://developer.okta.com/blog/2020/01/23/pkce-oauth2-spring-boot<br/>

# KAfka
https://developer.okta.com/blog/2020/01/22/kafka-microservices<br>

# PASETO Tokens
https://developer.okta.com/blog/2020/02/14/paseto-security-tokens-java<br/>

# Documenting spring controller
https://www.baeldung.com/spring-rest-openapi-documentation<br/>
https://stackoverflow.com/questions/61346751/can-we-replace-swagger-ui-with-redoc-in-springdoc<br/>


# building uisng github actions
https://developer.okta.com/blog/2020/05/18/travis-ci-to-github-actions<br/>

# code coverage
https://codecov.io/<br/>
https://codebeat.co/<br/>

# sonar cloud
https://sonarcloud.io/<br/>
https://spotbugs.github.io/<br/>
https://www.baeldung.com/pmd<br/>
https://www.baeldung.com/checkstyle-java<br/>

'
# code documentation
https://dzone.com/articles/best-practices-of-code-documentation-in-java<br/>
https://www.jrebel.com/blog/tips-and-tricks-for-better-java-documentation<br/>
https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html<br/>
https://medium.com/@rhamedy/a-short-summary-of-java-coding-best-practices-31283d0167d3<br/>
https://www.baeldung.com/javadoc<br/>
https://www.baeldung.com/java-clean-code<br/>

# Open Source Guides
https://opensource.guide/<br/>
https://opensource.org/<br/>


# Rules to live by for commit messages:

    Don’t end your commit message with a period.<br/>
    Keep your commit messages to 50 characters or less. Add extra detail in the extended description window if necessary. This is located just below the subject line.<br/>
    Use active voice. For example, "add" instead of "added" and "merge" instead of "merged".<br/>
    Think of your commit as expressing intent to introduce a change.<br/>
