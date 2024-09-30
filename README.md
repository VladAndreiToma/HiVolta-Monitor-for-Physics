HiVolta Monitor for Physics
HiVolta Monitor is an automated data extraction and monitoring software designed using Python, InfluxDB, Grafana, and Docker. This project began with the need to extract data from a CAEN module with a BIOS GUI, which previously relied on hardcoded terminal commands. The data communicated by this module is of significant interest and requires efficient monitoring.

Overview
The project is structured around a Docker Compose file that sets up two essential services:

InfluxDB: This time-series database automatically assigns timestamps to every entry, supports data injection as JSON objects, and allows for easy querying using SQL-like syntax.
Grafana: A powerful dashboard server that connects to the InfluxDB instance to visualize time-dependent data.
The Docker setup also includes binding volumes to ensure data persistence and backup, safeguarding against potential data loss.

Functionality
The core functionality of the system is driven by a Python script that:

Simulates terminal instructions in a Linux environment.
Connects to the target machine and creates a screen instance.
Initializes a Telnet communication request and executes commands to retrieve the data table.
Waits for the table to render and captures a "print screen" of the table to extract the data as raw text.
Processes the text file to extract relevant JSON entries, which are then injected into the InfluxDB.
From this point, Grafana can be easily configured to monitor and display the data of interest.

Features
Automated Data Extraction: Efficiently pulls data from the CAEN module.
Data Persistence: Ensures data is safely stored and backed up.
Dynamic Visualization: Grafana provides real-time insights into the data trends.
Easy Maintenance: The organized structure of the project allows for straightforward updates and improvements.
Thank you for your interest in this project!

Best regards,
Engr. Vlad Andrei Toma
Physicist @ Gamma Driven Experiments Department @ ELI-NP, Romania
