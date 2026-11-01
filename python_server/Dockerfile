FROM python:3.11@sha256:390127d66a75154671aa02f62a49aa7f83c386f33cdc84a8e8f060650e2e19f8

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
