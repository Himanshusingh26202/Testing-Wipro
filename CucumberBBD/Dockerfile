FROM maven:3.9.15-eclipse-temurin-21

RUN apt-get update && apt-get install -y \
    chromium \
    chromium-driver \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY . .

RUN mvn clean install -DskipTests

CMD ["mvn","-Dtest=Runner.RunCucumberTest","test"]
 