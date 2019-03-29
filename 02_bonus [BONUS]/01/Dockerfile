FROM debian

MAINTAINER bsharna <bsharna@student.21-school.ru>

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget default-jre

WORKDIR minecraft

RUN wget https://launcher.mojang.com/v1/objects/3737db93722a9e39eeada7c27e7aca28b144ffa7/server.jar

RUN echo ‘eula=true’ > eula.txt

EXPOSE 25565

ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar

#docker build -t 01 .

#docker run -d -p 25565:25565 01
