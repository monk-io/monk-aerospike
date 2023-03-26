# Aerospike & Monk
This repository contains Monk.io template to deploy Aerospike either locally or on cloud of your choice (AWS, GCP, Azure, Digital Ocean).

# Prerequisites
- [Install Monk](https://docs.monk.io/docs/get-monk)
- [Register and Login Monk](https://docs.monk.io/docs/acc-and-auth)
- [Add Cloud Provider](https://docs.monk.io/docs/cloud-provider)
- [Add Instance](https://docs.monk.io/docs/multi-cloud)

#### Make sure monkd is running.
```bash
foo@bar:~$ monk status
daemon: ready
auth: logged in
not connected to cluster
```

## Clone Repository
```bash
git clone https://github.com/monk-io/monk-aerospike
```

## Load Template
```bash
cd monk-aerospike
monk load MANIFEST
```


#### Let's take a look at the themes I have installed.
```bash
foo@bar:~$ monk list aerospike
✔ Got the list
Type      Template             Repository  Version  Tags
runnable  aerospike/aerospike  local       -        -
```

## Deploy Stack
```bash
foo@bar:~$ monk run aerospike/aerospike
```

## Variables
The variables are in `griddb.yml` file. You can quickly setup by editing the values here.

| Variable     | Description      | Default      |
|--------------|------------------|--------------|
| image_tag    | Docker image tag | ce-6.2.0.7_1 |
| service_port | Service port     | 3000         |

## Stop, remove and clean up workloads and templates

```bash
monk purge -a
```

