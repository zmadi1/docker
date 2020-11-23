FROM debian


ENV TS3SERVER_LICENSE=accept
#Accepts the teamspeak license

WORKDIR /home/teamspeak

EXPOSE 1098/udp 1819 9101

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget bzip2 && \
	wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2  && \
	tar xvf *.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

#docker run --rm -p 1098:1098/udp -p 1819:1819 -p 9101:1901 teamspeaker
