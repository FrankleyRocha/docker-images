FROM ubuntu:18.04

RUN apt update
RUN apt install -y curl wget vim zip unzip git build-essential
RUN apt install -y openjdk-17-jdk libswt-gtk-4-java
RUN apt install -y zsh
RUN apt install -y python python-pip python3 python3-pip

RUN usermod --shell /usr/bin/zsh root
ENV SHELL=/bin/zsh
SHELL [ "/bin/zsh", "-c" ]

RUN /bin/sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
RUN sed -i 's/ZSH_THEME="robbyrussell"/ZSH_THEME="bira"/' ~/.zshrc

ENTRYPOINT ["/bin/zsh"]
#CMD ["/bin/zsh"]
