FROM maven AS build

WORKDIR /app

COPY /target/*.war /app


FROM tomcat 

COPY --from=build /app/*.war /usr/local/tomcat/webapps/

EXPOSE 8081
