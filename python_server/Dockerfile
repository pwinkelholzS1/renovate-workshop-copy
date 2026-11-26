FROM python:3.15@sha256:e4bc83a3314d078d651f06c8440e9a03ba892ee2f6577437f174abd8731fb343

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
