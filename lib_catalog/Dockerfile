FROM python:3.8-slim
WORKDIR /code
RUN adduser python && chown -R python /code
USER python
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r requirements.txt
CMD python manage.py migrate
COPY . .
