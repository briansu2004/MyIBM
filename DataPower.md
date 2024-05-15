# IBM DataPower

- [DataPower Docker Image](#datapower-docker-image)

IBM DataPower Gateway is a purpose-built security and integration platform for mobile, cloud, API, web, SOA, and B2B workloads. It provides a comprehensive set of security and integration capabilities to help organizations streamline their IT infrastructure and improve their agility in responding to business needs.

Some key features and capabilities of IBM DataPower include:

1. Security: DataPower provides robust security features such as access control, threat protection, encryption, and authentication to safeguard sensitive data and protect against cyber threats.

2. Integration: It offers powerful integration capabilities to connect disparate systems, applications, and data sources, enabling seamless communication and data exchange across the enterprise.

3. Transformation: DataPower supports data transformation and manipulation tasks, including message transformation, protocol conversion, and data format normalization, to ensure compatibility between different systems and interfaces.

4. Policy-based control: Administrators can define and enforce policies to govern the behavior of traffic flowing through DataPower, ensuring compliance with regulatory requirements and organizational standards.

5. Performance and scalability: DataPower is designed for high performance and scalability, capable of handling large volumes of transactions and supporting mission-critical workloads with low latency and high throughput.

6. Monitoring and management: It provides comprehensive monitoring and management capabilities, including real-time visibility into traffic, performance metrics, and centralized administration through a web-based interface or command-line interface (CLI).

IBM DataPower Gateway plays a crucial role in enabling secure and efficient communication and integration within complex enterprise architectures, helping organizations achieve greater agility, flexibility, and reliability in their IT infrastructure.

## DataPower Docker Image

```dos
docker login cp.icr.io -u cp -p myEntitlementKey

docker pull ibmcom/datapower:latest

docker pull icr.io/cpopen/datapower/datapower-limited:10.5.0.5
docker pull icr.io/appc-dev/ace-server:latest
docker pull icr.io/ibm-messaging/mq:9.3.2.1-r2-amd64
docker pull icr.io/appcafe/open-liberty:23.0.0.5-kernel-slim-java8-openj9-ubi-amd64
```

<!-- ```dos
docker run -it -e DATAPOWER_ACCEPT_LICENSE=true -e DATAPOWER_INTERACTIVE=true -p 9099:9099 --name DataPowerInWin ibmcom/datapower

docker run -d -p 2200:22 -p 9090:9090 --name unit-test registry.ng.bluemix.net/hstenzel/datapower-sample
``` -->

<!-- docker run -it -v $PWD/config:/drouter/config -v $PWD/local:/drouter/local -e DATAPOWER_ACCEPT_LICENSE=true -e DATAPOWER_INTERACTIVE=true -p 9099:9099 --name DataPowerInWin ibmcom/datapower -->

Unix

```shell
docker run -it –-name name \
-v $(pwd)/config:/opt/ibm/datapower/drouter/config \
-v $(pwd)/local:/opt/ibm/datapower/drouter/local \
-v $(pwd)/certs:/opt/ibm/datapower/root/secure/usrcerts \
-e DATAPOWER_ACCEPT_LICENSE="true" \
-e DATAPOWER_INTERACTIVE="true" \
-p 9090:9090 \
tag
```

`https://github.com/ibm-datapower/datapower-tutorials`
