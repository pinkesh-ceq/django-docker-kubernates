FROM python:3.9.13-alpine3.14

WORKDIR /usr/src/app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip 
COPY ./requirements.txt /usr/src/app
RUN pip install -r requirements.txt

# COPY api_app /usr/src/app
# COPY ./api_app /usr/src/app
# COPY ./ApiProject /usr/src/app
# COPY ./db.sqlite3 /usr/src/app
# COPY ./manage.py /usr/src/app
# COPY ./Dockerfile /usr/src/app
# COPY ./kubernates /usr/src/app/

COPY . /usr/src/app

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]