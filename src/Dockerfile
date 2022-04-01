FROM python:3.11.0a6-bullseye
WORKDIR /app
COPY requirements.txt /app 
RUN python -m pip install -r requirements.txt
COPY . /app
EXPOSE 5000
CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:5000" , "-c", "config-py", "app:app"]
