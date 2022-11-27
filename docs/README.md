# Inno Broker API Manual

The main service contributed by the ROSE-AP is automated planning, to minimize the up-front automated robotic cell productivity 

## Contents

-   [Requirements](#requirements)
-   [Configuration](#configuration)
-   [Usage](#usage)
-   [License](#license)

## Requirements

In order to utilize the product [.net5](https://dotnet.microsoft.com/en-us/download/dotnet/5.0) framework or higher needs to be installed on the same machine with the docker.

## Configuration

All configrations are done in the settings page of the broker.

<img width="200" alt="settings" src="docs/img/ettings.png">

PLC Ip: is the IP of the programable controller which drives the robot cell and gathers the data.
Server Ip: is the IP of the docker image with the Crate data base.
User: Username to access the db.
Pw: Password to access the db.
Production Table: Is the table from the CrateDB where the production data will be stored.
Part Table: Is the table from the CrateDB where the parts data will be stored.

*Optional it can be added to run automaticaly at startup. 

## Usage

<img width="1000" alt="interface" src="docs/img/interface.png">

When all steps of the Broker and databse configration are done the broker can be started.
First Step is to Connect, by this we establish a connection with the PLC. If not succesfull an error will be thrown in the logfile.
From the PLC the following commands are definde in order to exchange the date: 0-Waiting Trigger; 1-Trigger WLine; 2-Trigger WPart; 100-WLine Error; 101-WPart Error Bussy-255
The rest of the date that is sent from and to the PLC is displayed on the interface of the api in realtime.

## License
The Inno West Rose-AP components are licensed under [Apache 2.0](/LICENSE) © 2022 Inno Robotics S.R.L.
