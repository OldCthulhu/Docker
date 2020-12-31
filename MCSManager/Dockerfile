FROM mamohr/centos-java

WORKDIR /home
RUN yum install wget -y
RUN wget https://nodejs.org/dist/v15.5.0/node-v15.5.0-linux-x64.tar.gz
RUN tar -zxvf node-v15.5.0-linux-x64.tar.gz
RUN ln -s $(pwd)/node-v15.5.0-linux-x64/bin/node /usr/bin/node
RUN ln -s $(pwd)/node-v15.5.0-linux-x64/bin/npm /usr/bin/npm
RUN yum install git -y
RUN git clone https://github.com/Suwings/MCSManager.git
WORKDIR /home/MCSManager
RUN npm install

EXPOSE 23333
VOLUME [/home/MCSManager]

CMD ["/usr/bin/node", "app.js"]
