FROM python:3.3 as poll

WORKDIR /home/popeye/poll

COPY requirements.txt ./

RUN pip3 install -r requirements.txt

EXPOSE 80

COPY . .

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
