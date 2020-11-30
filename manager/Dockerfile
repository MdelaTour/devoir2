FROM python:3.8.6

RUN pip install os-win
RUN pip install psycopg2
#RUN pip install unittest
RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
	RUN chmod +x /wait-for-it.sh
	ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]
RUN mkdir /manager

ADD __main__.py .

COPY . ./manager

 #define a startup cmd
CMD ["python", "-m", "manager"]

VOLUME ["/data-volume"]