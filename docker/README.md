# Inno-West
 ROSE-AP automated planning

# Docker Image
This project is part of [DIH2](http://www.dih-squared.eu/). For more information check the RAMP Catalogue entry for the [components](https://github.com/xxx).
 ## Contents

-   [Background](#background)
-   [Requirements](#requirements)
-   [Install](#install)
-   [Usage](#usage)
-   [License](#license)

## Background

CrateDB is utilized for data collection.

## Requirements

Requires [docker](https://github.com/docker) preinstalled.

## Installation

[Orion Context Broker](https://github.com/telefonicaid/fiware-orion/tree/master/docker)
To do this run this command

.. code-block:: console
sudo docker run -d --name orion1 -p 1026:1026 fiware/orion

[CrateDB](https://github.com/crate/crate)
To do this run this command

.. code-block:: console
sh$ docker run --publish 4200:4200 --publish 5432:5432 crate -Cdiscovery.type=single-node

## License
The INNO WEST ROSE-AP components are licensed under [Apache 2.0](/LICENSE) © 2022 INNO ROBOTICS S.R.L.
