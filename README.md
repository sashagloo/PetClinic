
# PetClinic project

free interpretation of https://github.com/spring-petclinic

#INIT
------------------------------------
    DevTools
    Lombok
    Web
    Thymeleaf
    JPA / Spring Data JPA / Spring ORM / Hibernate
    MySQL JDBC driver
    H2 db (with embedded support)
    Actuator

Layers
------------------------------------
    View:       Thymeleaf
                webjars
                JSP with custom tags
                CSS Bootstrap 
                LESS customised
    Controller: Spring MVC
                Bean validation
    Service:    @Cacheable
                @Transactional
    Repository: Spring Data JPA
                JPA
                JDBC
    Containers support: Tomcat / Jetty embbeded 
                
Database
------------------------------------
    HSQLDB / MySQL / PostgreSQL support
    Maven config
    DDL / DML SQL scripts for each database vendor in !>>> data-access.properties
        :   jdbc.initLocation=classpath:db/${db.script}/initDB.sql
        :   jdbc.dataLocation=classpath:db/${db.script}/populateDB.sql
            
    
    
RUN
------------------------- -----------
    docker run --name muysql-petclinic -e MYSQL_ROOT_PASSWORD-petclinic -e MUYSQL_DATABASE=petclinic
    mvn tomcat7:run-war -P MySQL


Unit Testing
------------------------------------
    Spring Test / JUnit / HSQLDB / Mockito / AssertJ / Hamcrest / Json Path
               