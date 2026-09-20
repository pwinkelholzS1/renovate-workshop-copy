FROM python:3.11@sha256:70e8e937c1da72df1688e883a2108b0feff03381187fa78eca6d9b10df411320

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
