FROM python:3.11@sha256:1829edfddfa93b381f575e89221003055b9a0b6cf03dfe786edd798bb6817e83

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
