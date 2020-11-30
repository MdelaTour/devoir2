FROM python:3.8.6

RUN pip install os-win
RUN pip install psycopg2
#RUN pip install unittest
RUN mkdir /manager
RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
	RUN chmod +x /wait-for-it.sh
	ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]
ADD __main__.py .

COPY . ./manager

 #define a startup cmd
CMD ["python", "-m", "manager"]

VOLUME ["/data-volume"]

EXPOSE 5000