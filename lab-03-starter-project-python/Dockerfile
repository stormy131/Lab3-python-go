FROM python:3.10-alpine

WORKDIR /app
COPY . .

RUN apk add build-base
RUN python -m venv ./.venv
RUN . ./.venv/bin/activate
RUN pip install -r requirements/backend.in

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"]