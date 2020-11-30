#réutilisation d'image existante
FROM python:3.8.6

#run additional cmd
RUN pip install pandas
RUN pip install flask
WORKDIR /manager/
ADD __main__.py .

 #define a startup cmd
CMD ["python", "__main__.py"]

VOLUME ["/data-volume"]

EXPOSE 5000