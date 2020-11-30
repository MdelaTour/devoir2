#réutilisation d'image existante
FROM python:3.8.6

#run additional cmd
RUN pip install os-sys
RUN pip install psycopg2
WORKDIR /manager/
ADD __main__.py .

COPY . ./file

 #define a startup cmd
CMD ["python", "__main__.py"]

VOLUME ["/data-volume"]

EXPOSE 5000