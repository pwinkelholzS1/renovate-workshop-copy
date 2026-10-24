FROM python:3.11@sha256:8f6593e62e991b818dc28750c0c67c340046a70ab5cf79df52116005ec9cbf56

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
