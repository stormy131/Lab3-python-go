FROM python:3.10-buster

WORKDIR /app

COPY ./requirements/backend.in /app/requirements/backend.in

COPY ./build/index.html /app/build/index.html
COPY ./spaceship /app/spaceship
RUN python -m venv ./.venv
RUN . ./.venv/bin/activate
RUN pip install -r requirements/backend.in

CMD ["uvicorn", "spaceship.main:app", "--host=0.0.0.0", "--port=8080"]