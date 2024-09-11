FROM python:3.12
WORKDIR /usr/src/app
COPY ./app/. ./
ARG NO_CACHE
RUN if [ "$NO_CACHE" = "true" ]; then echo "No cache"; fi
RUN pip install -r requirements.txt
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "$PORT"]
