FROM openjdk:11-jre-slim

RUN apt-get update && apt-get install -y wget

RUN mkdir /opt/plantuml
WORKDIR /opt/plantuml

RUN wget https://netcologne.dl.sourceforge.net/project/plantuml/plantuml.jar

CMD ["java", "-jar", "plantuml.jar", "-tsvg"]
