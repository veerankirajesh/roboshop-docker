FROM python:3.9.22-alpine3.21

EXPOSE 8080
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123
USER root
WORKDIR /app
COPY requirements.txt /app/
RUN apk add python3-dev build-base linux-headers pcre-dev   # run pip install -r reqirements.txt
RUN pip install -r requirements.txt
COPY *.py /app/
COPY payment.ini /app/
#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]