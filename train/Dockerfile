# FROM pytorch/pytorch:latest
FROM python:3

WORKDIR /app

ADD requirements.txt /app

RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt 


RUN mkdir /model
VOLUME /model
ENV MODEL_DIR /model


# do this last since ill be changing this most frequently as i develop
ADD train.py /app


# Run the service
CMD [ "python3", "train.py" ]


# docker build -t train .
# docker run -it train
