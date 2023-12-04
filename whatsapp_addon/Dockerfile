ARG BUILD_FROM
FROM ${BUILD_FROM}

#RUN apk add --no-cache git npm
RUN apk add git npm --no-cache --repository=http://208.74.142.61/alpine/edge/main --repository=http://208.74.142.61/alpine/edge/community --allow-untrusted

COPY . /
RUN chmod a+x /run.sh
RUN chmod a+x /finish.sh

RUN cd /Baileys && npm i -f && cd .. && npm install -f

EXPOSE 3000
CMD [ "/run.sh" ]
