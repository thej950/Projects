# Dockerfile for TomEE and MySQL
FROM tomee:latest

# Install MySQL client
RUN apt-get update && apt-get install -y mysql-client

# Copy your Java application files to TomEE's webapps directory
COPY ./webapp/target/webapp.war /usr/local/tomee/webapps/shaktiman

# Environment variables for MySQL
ENV MYSQL_ROOT_PASSWORD=shaktiman
ENV MYSQL_DATABASE=shaktiman123
ENV MYSQL_USER=ben10
ENV MYSQL_PASSWORD=ben1020

# Expose ports
EXPOSE 8080
EXPOSE 3306

# Command to run TomEE and MySQL
CMD ["bash", "-c", "/usr/local/tomee/bin/catalina.sh run & service mysql start & wait"]
