FROM python:3.15@sha256:9b99a39a1659e8a507603edfad004c8e33d1855c70a15f2024861bd98ae19416

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
