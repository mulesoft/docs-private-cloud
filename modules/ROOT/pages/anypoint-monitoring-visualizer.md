= Anypoint Monitoring and Visualizer
ifndef::env-site,env-github[]
include::_attributes.adoc[]
endif::[]

Anypoint Monitoring

== Overall Architecture

Anypoint Monitoring is an optional feature during installation, which includes Anypoint Visualizer. Both products require 3 dedicated nodes, normally labeled *amv_node*.

In those 3 nodes, the following Helm charts will be installed in 4 different namespaces:

. `dias`

.. dias-prov-k8s-am-influxdb-comp
.. dias-prov-k8s-am-ingestor-comp
.. dias-prov-k8s-amr-certs-comp
.. dias-prov-k8s-amr-ingestor-router-comp
.. dias-prov-k8s-insight-comp
.. dias-provisioning-api

. `monitoring-center`

.. monitoring-center-alerts-api
.. monitoring-center-metrics-api
.. monitoring-center-settings-api
.. monitoring-center-ui
.. monitoring-center-ui-api
.. monitoring-center-visualizer

. `default`

.. stolon-amv

. `visualizer`
.. visualizer-experience-api
.. visualizer-janitor
.. visualizer-topology-api
.. visualizer-topology-processor
.. visualizer-ui

It's important to mentioned that a dedicated Stolon DB will be deployed in addition to the one used by the platform.



self-signed certs

== Requirements

hardware, ports, certs


== Restore/Backup

required size

----
openssl dhparam 2048 -out dhparam.pem
----
