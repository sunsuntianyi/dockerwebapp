FROM node:latest

COPY . /

WORKDIR /

RUN apt-get update && \
    apt-get install -y \
        python \
        python-pip \
        python-dev \
        python-setuptools \
        groff \
        less \
    && pip install --upgrade pip \
    && apt-get clean

RUN pip --no-cache-dir install --upgrade six

RUN pip --no-cache-dir install --upgrade grpcio grpcio-tools

RUN pip --no-cache-dir install -U tensorflow

RUN npm install --production

EXPOSE 3000

CMD npm start