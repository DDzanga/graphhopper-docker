
# GraphHopper router backend using Docker

## Installation

- [Install Docker](https://docs.docker.com/get-docker/)
- Clone this repository

## Activation 🚗🚶🏼‍♂️🚲

Navigate to the folder you just cloned and run `docker-compose up -d`

By default this repository sets up routing for Jamaica. You can those by editing the file names on the `gh-update.bat` file and the `docker-compose.yml` file accordingly. The default settings use car, foot, biking and hiking as travel modes. Change those in the `gh-config.yml` file.


## Updating the routing data 🌎🌍🌏

For quick activation, the server will initially use historic routing data.
To use up-to-date routing data, run `./gh-update.sh` on Linux or `gh-update.bat` on Windows.

The scripts are identical (hard linked) and perform the following tasks:
  - Download new OSM data if needed
  - Calculate new routing data
  - Start or restart the GraphHopper server, as appropriate, with the new routing data

The scripts can also be run periodically or after changing the `gh-config.yml` file.

## Read more about GraphHopper

👉🏼 https://www.graphhopper.com/open-source/