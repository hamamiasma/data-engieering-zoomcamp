'''FROM python:3.13.11-slim

RUN pip install pandas pyarrow

WORKDIR /app
COPY pipeline.py pipeline.py

ENTRYPOINT ["python", "pipeline.py"]'''

docker run -it --rm \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v ny_taxi_postgres_data:/var/lib/postgresql \
  -p 5432:5432 \
  postgres:18