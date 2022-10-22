FROM python:3.10

RUN pip install --upgrade pip

COPY requirements.txt /stocks_products/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /stocks_products/requirements.txt

COPY . /stocks_products

EXPOSE 88

WORKDIR stocks_products

RUN python3 manage.py makemigrations

RUN python3 manage.py migrate

CMD ["python3", "manage.py", "runserver", "0.0.0.0:88"]
