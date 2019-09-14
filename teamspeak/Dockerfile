FROM debian:latest

LABEL maintainer=tstephen@student.wethinkcode.co.za
LABEL status=unmaintainable

RUN apt update && \
	apt install -y wget bzip2 && \
	wget https://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2 && \
	tar -xvf teamspeak3-server_linux_amd64-3.9.1.tar.bz2

WORKDIR /teamspeak3-server_linux_amd64

EXPOSE 9987/udp 10011/tcp 30033/tcp

ENV TS3SERVER_LICENSE="accept"

ENTRYPOINT ["./ts3server_minimal_runscript.sh"]

CMD ["start"]