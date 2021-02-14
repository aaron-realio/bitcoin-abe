FROM python:2-alpine

# install python
RUN apk update && apk add --no-cache bash openssl-dev openssl libffi-dev build-base postgresql-libs musl-dev postgresql-dev curl git

WORKDIR /bitcoin-abe

COPY . .

RUN pip install -r requirements.txt

RUN python setup.py install

EXPOSE 80

ENV PATH=$PATH:/bitcoin-abe

CMD ["python"]
