
FROM debian:buster

RUN apt-get update \
	&& apt-get install -y curl gnupg

RUN curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
  chmod 755 msfinstall && \
  ./msfinstall

CMD ["msfconsole"]
