# Usamos imagen base con JDK
FROM eclipse-temurin:17-jdk-alpine

# Directorio de trabajo
WORKDIR /app

# Copiamos archivos de proyecto
COPY . .

# Construimos el proyecto usando Maven Wrapper
RUN ./mvnw clean package -DskipTests

# Exponemos el puerto que usa Spring Boot
EXPOSE 8080

# Ejecutamos la app
CMD ["java", "-jar", "target/conexionbd-0.0.1-SNAPSHOT.jar"]
