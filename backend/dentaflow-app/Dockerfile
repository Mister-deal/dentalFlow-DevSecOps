# Étape 1 : Build Maven
FROM maven:3.9.2-eclipse-temurin-20 AS build
WORKDIR /app

# Copier uniquement les fichiers nécessaires pour le build
COPY ../pom.xml ../dentaflow-core/pom.xml ../dentaflow-client/pom.xml ../dentaflow-app/pom.xml ./
COPY ../dentaflow-core ./dentaflow-core
COPY ../dentaflow-client ./dentaflow-client
COPY ../dentaflow-app ./dentaflow-app

# Build du jar avec skip des tests
RUN mvn clean package -DskipTests

# Étape 2 : Image finale minimale
FROM eclipse-temurin:20-jre-alpine
WORKDIR /app

# Copier uniquement le jar final
COPY --from=build /app/dentaflow-app/target/dentaflow-app.jar ./dentaflow-app.jar

# Exposer le port
EXPOSE 8080

# Lancer l'application
ENTRYPOINT ["java", "-jar", "dentaflow-app.jar"]