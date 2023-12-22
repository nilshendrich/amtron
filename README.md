# Inofficial AMTRON API documentation

## Introduction

This repo contains a reverse-engineered documentation for the REST Api of a Mennekes Amtron
EV-Charger equipped with Networking.

The information provided here was retrieved using the ChargeApp on Android and the Amtron Xtra 11 C2.

**It may not be applicable to other Amtron chargers.**

## Amtron API

### General Information

* The **DevKey required for each request** can be found in the documents you received with your Wallbox.
In the document it is called **APP-Pin**.
* Every request has to have the header param `Accept: application/json`.
* Every path shown below has a base url of `http://amtron-ip:25000/MHCP`
* Useful information can be found at the bottom of every page under **Notes**.
* Amtron Wallboxes dont like to be stressed with requests. Dont overdo it.

### Documentation

#### API Version 1.0

* [Get Device Information](./docs/api/DevInfo/get.md): `GET /1.0/DevInfo`
* [Set Device Information](./docs/api/DevInfo/post.md): `POST /1.0/DevInfo`

* [Get Charging Information](./docs/api/ChargeData/get.md): `GET /1.0/ChargeData`
* [Set Charging Information](./docs/api/ChargeData/post.md): `POST /1.0/ChargeData`

* [Set EnergyManager parameters](./docs/api/HomeManager/post.md): `POST /1.0/HomeManager`

* [Set Tariff Data Parameters](./docs/api/TariffData/post.md): `POST /1.0/TariffData`
* [Set Tariff Data Parameters](./docs/api/TariffData/post.md): `POST /1.0/TariffData`

#### API Version 1.1

* [Get Other Information](./docs/api/Info/get.md) `GET /1.1/*`
