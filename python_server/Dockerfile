FROM python:3.11@sha256:8ce0c4b7bad2a0939d3fe311e30f1f12b491b0ba335fe1f2daa1b99894588503

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
