#Docker Best Practises implemented
FROM node:20.15.0-alpine3.20 
EXPOSE 8080
ENV DB_HOST=mysql
RUN addgroup -S expense && adduser -S expense -G expense \
    && mkdir /opt/server \
    && chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js /opt/server/
RUN npm install
USER expense
EXPOSE 8081
CMD [ "node", "index.js" ]

#alpine is the OS, on top it nodejs application implemented.

# FROM node:20
# EXPOSE 8080
# ENV DB_HOST=mysql
# RUN useradd expense
# RUN mkdir /opt/server
# RUN chown expense:expense -R /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD [ "node", "index.js" ]