FROM python:3.12.0-alpine

COPY sa /app
WORKDIR /app
RUN pip3 install -r requirements.txt && \
    python3 -m textblob.download_corpora

EXPOSE 5000

ENTRYPOINT ["python3"]

CMD ["host-details.py"] --bind :$PORT=5000
ENV ContainerPort=5000
