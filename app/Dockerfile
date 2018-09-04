FROM alpine:3.7

RUN mkdir /API_Fresco

RUN apk update \
  && apk add --no-cache python3 \
  && apk add libc-dev \
  && apk --no-cache --update-cache add gcc gfortran build-base python3-dev wget freetype-dev libpng-dev openblas-dev \	
  && apk add --no-cache subversion \
  && apk add curl bash binutils tar git \
  && python3 -m ensurepip \
  && git clone https://github.com/monika412/API_Fresco/ /API_Fresco \
  && pip3 install -r /API_Fresco/requirements.txt 	

VOLUME ["/API_Fresco"]

#ADD wait-for-it/wait-for-it.sh /wait-for-it.sh

#RUN chmod +x /wait-for-it.sh

#ENTRYPOINT [ "/wait-for-it.sh", "db:9042", "--" ]


CMD sleep 200 && cd /API_Fresco && git pull && python3 /API_Fresco/FrescoAPI.py

