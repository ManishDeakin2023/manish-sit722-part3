FROM python:slim-buster

WORKDIR /app

COPY ./app/. ./
COPY requirements.txt ./

ARG NO_CACHE
RUN if [ "$NO_CACHE" = "true" ]; then echo "No cache"; fi

RUN pip install --no-cache-dir -r requirements.txt

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "$PORT"]
