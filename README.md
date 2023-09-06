# Apache Kafka® and Python tutorial


The Apache Kafka® and Python tutorial aims at showcasing the basics of working with Apache Kafka® and Python using a series of notebooks in the main folder.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Aiven-Labs/python-apache-kafka-tutorial)

## Overview


The tutorial contains the following sections:

* Create an Apache Kafka cluster with Aiven
* Producing data to Apache Kafka
* Consuming data from Apache Kafka
* Concurrent Consumers from a topic
* Multiple Applications consuming from a topic

## Setup


The tutorial requires the Access to an Apache Kafka® cluster.
If you don't have one, you can create it with [Aiven](https://go.aiven.io/ft-signup-kafka-python), using the free trial. 


### Create an Apache Kafka cluster with Aiven

You can create an Aiven for Apache Kafka service by:

* Navigating to the [Aiven website](https://go.aiven.io/ft-signup-kafka-python) and creating an account
* Clicking on **Create service**
* Selecting **Apache Kafka**
* Selecting the cloud vendor and region
* Selecting the plan (a **Business-4** plan would be enough)
* Clicking on **Create service**

After a couple of minutes, the Aiven for Apache Kafka service will be ready to use.

### Run the notebooks folder with Jupyterlab on Docker

You need to have Docker installed. Once you do, clone the repository with:

```bash
git clone https://github.com/Aiven-Labs/python-apache-kafka-tutorial
```

Navigate to the `python-apache-kafka-tutorial` with

```bash
cd python-apache-kafka-tutorial
```

Run the following to start JupyterLab on Docker

```
docker run                      \
    --rm -p 8888:8888           \
    -e JUPYTER_ENABLE_LAB=yes   \
     -v "$PWD":/home/jovyan/work jupyter/datascience-notebook
```

The above command will start a container with JupyterLab and map the current folder in the notebook. In the terminal where the code is executed you'll see appearing a URL like the below:

```
Or copy and paste one of these URLs:
        http://1a103b1d8d2b:8888/lab?token=XYZ
        http://127.0.0.1:8888/lab?token=XYZ
```

Use the `127.0.0.1` URL to access the JupyterLab environment

### Download the required SSL certificates

The SSL certificates are used to securely connect the Python clients and the Apache Kafka cluster. To download them:

* In the Aiven Console, navigate to the Aiven for Apache Kafka cluster created
* Download the:
    * Access Key
    * Access Certificate
    * CA Certificate

Once downloaded the certificates, you can move them in the [sslcerts](sslcerts) folder.




## License

Apache Kafka® and Python tutorial is licensed under the Apache license, version 2.0. Full license text is available in the [LICENSE](LICENSE) file.

Please note that the project explicitly does not require a CLA (Contributor License Agreement) from its contributors.

## Contact

Bug reports and patches are very welcome, please post them as GitHub issues and pull requests at https://github.com/aiven/{{PROJECT_NAME}} . 
To report any possible vulnerabilities or other serious issues please see our [security](SECURITY.md) policy.
