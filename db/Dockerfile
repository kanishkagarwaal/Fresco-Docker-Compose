FROM datastax/dse-server

RUN mkdir /tmp/cass_DB

RUN cd /tmp/cass_DB && git clone https://github.com/monika412/Cassandra_Fresco.git

RUN chmod +x /tmp/cass_DB/Cassandra_Fresco/scripts/run_db_scripts.sh

#RUN /tmp/cass_DB/Cassandra_Fresco/scripts/run_db_scripts.sh
#RUN sh /tmp/cass_DB/Cassandra_Fresco/scripts/run_db_scripts.sh

ENTRYPOINT /bin/sh /tmp/cass_DB/Cassandra_Fresco/scripts/run_db_scripts.sh

#ENTRYPOINT ["/tmp/cass_DB/Cassandra_Fresco/scripts/run_db_scripts.sh"]

#CMD /bin/shdocker 
