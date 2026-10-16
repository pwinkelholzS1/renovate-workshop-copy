FROM python:3.11@sha256:50cfccc707e8721201ee018bfd7f6a85d8eacf49c4f9f75833a2aba09a10411f

WORKDIR /app
COPY requirements.txt ./
COPY src/ ./src

RUN pip install -r requirements.txt

COPY quotes.txt ./quotes.txt
COPY quotes.txt ./src/quotes.txt
COPY start.sh ./

EXPOSE 8002

CMD ["./start.sh"]
