# HiVolta-Monitor-for-Physics
a software dedicated in automated data extraction and monitoring using python , influxdb , grafana and docker
All started when data was needed from a CAEN module with bios gui,  hardcoded availalbe on the terminal. Data communicated by the module is of very high interest.
What am I doing here is to set up a docker composer file that will source 2 services that I need: one influx database( it has automatically asigned timestamps to every entry , supports injection of data as json objects and also is easily queried using SQL instructions ) and a grafana dashboard server that is connected to the database and dipslay data of interest with time dependency also sourced from the docker file. The docker file also creates binding volumes to the containers so I ensure data persistency and backup in case of something wrong happening.
The python script deploys some jobs that simulate terminal instructions in linux. It connects to target machine creating a screen instance , then initializes a telnet communication request, executes some commands to get the data table, waits for the table to render and then makes a hardcopy that is a "printscreen" of the table to get data as raw text. Text file is then brushed to obtain the relevant jsons that will be put in the database, from there grafana monitoring is set up easily. 
Everything is smooth , efficient and well organized , making everything easy to maintain.
With best regards,
Engr. Vlad Andrei Toma , Physicist @ Gamma Driven Experiments Departament @ ELI-NP . Ro
