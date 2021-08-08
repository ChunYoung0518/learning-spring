#To use embeded database you will need:
1. /Users/dyoung/priceless/learning-spring/src/main/resources/data.sql
2. /Users/dyoung/priceless/learning-spring/src/main/resources/schema.sql
3. commen out the following lines in: /Users/dyoung/priceless/learning-spring/src/main/resources/application.properties
spring.jpa.database=postgresql
spring.datasource.Platform=postgres
spring.datasource.setPlatform=postgres
spring.datasource.url=jdbc:postgresql://localhost:5432/dev
spring.datasource.username=postgres
spring.datasource.password=postgres
4. Import com.h2database dependency and remove org.postgresql dependency

#To use remote database you will need:
1. cd /Users/dyoung/priceless/learning-spring/bin and run: ./start_postgresh.sh
2. Import org.postgresql dependency and remove com.h2database dependency
3. Need the following configuration in: /Users/dyoung/priceless/learning-spring/src/main/resources/application.properties
   
logging.level.org.hibernate.engine.jdbc.env.internal.LobCreatorBuilderImpl=error

spring.jpa.database=postgresql
spring.datasource.Platform=postgres
spring.datasource.setPlatform=postgres
spring.datasource.url=jdbc:postgresql://localhost:5432/dev
spring.datasource.username=postgres
spring.datasource.password=postgres