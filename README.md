# Data viewer

Data preview widget from csv files

---

## Summary

In order to share and highlight all the resources of this repo, it was proposed to create a digital tool of the "widget" type: `datami`. Indeed, a tool of this type allows to integrate on third-party sites (partner sites or others) a more or less large selection of resources. This solution allows both to avoid partner sites from "copying and pasting" the resources, to display on these third-party sites the resources always up to date, and to allow third-party sites as well as the source site to gain visibility, legitimacy and quality of information.

The other advantage of this solution is that it is only deployed once, but that the widget can be integrated and configured/customized on as many third-party sites as desired... for free.

The solution proposed and implemented here is based on an open source project supported by the digital cooperative [**multi**](https://multi.coop): the [Datami](https://datami.multi.coop) project.

---

## Demo

<!-- - Demo html page: [![Netlify Status](https://api.netlify.com/api/v1/badges/ac24c6a6-9abd-4e5a-bdcb-688c525840aa/deploy-status)](https://app.netlify.com/sites/datami-demo-ping-tiers-lieux/deploys)
- demo url: https://datami-demo-ping-tiers-lieux.netlify.app -->

---

## To go further

### Datami

The widget is an integral part of the [Datami](https://gitlab.com/multi-coop/datami) project

### Technical documentation

A site dedicated to Datami technical documentation can be consulted here: https://datami-docs.multi.coop

---

## Mini server for local development

A mini server is writen in the `server.py` to serve this folder's files.

To install the mini-server :

```sh
pip install --upgrade pip
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

or

```sh
sh setup.sh
source venv/bin/activate
```

---

### Run local server

To run the server on `http://localhost:8810`:

```sh
python server.py
```

or

```sh
sh run_server.sh
```

Files will be locally served on :

- `http://localhost:8810/content/<path:folder_path>/<string:filename>`
- `http://localhost:8810/statics/<path:folder_path>/<string:filename>`

---

## Crédits

| | logo | url |
| :-: | :-: | :-: |
| **Les Interconnectés** | ![Interconnectés](./images/interconnectes-logo.jpg) | https://www.interconnectes.com/ |
