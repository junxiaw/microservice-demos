FROM 192.168.1.52/system_containers/oraclejdk:8u192

MAINTAINER sparkxiong shi.xiong@tenxcloud.com

ENV PROFILE=test \
    NACOS_ADDR=spring-cloud-discovery.system-tmf-sharedns:8848 \
    NACOS_NAMESPACE=public \
    NACOS_GROUP=DEFAULT_GROUP \
    PAAS_NS=deafult \
    NACOS_USERNAME=nacos \
    NACOS_PASSWORD=nacos \
    MESH_SWITCHER_MESH=false\
    DEPLOY_TYPE=vm\
    MESH_SVC_NAME=cloud-provider-nacos204\
    JVM="-Xms256m -Xmx1g -XX:+UnlockExperimentalVMOptions -XX:+UseCGroupMemoryLimitForHeap -Djava.security.egd=file:/dev/./urandom"

ADD *.jar /app/app.jar

WORKDIR "/app"

EXPOSE 6666

CMD java -jar /app/app.jar
