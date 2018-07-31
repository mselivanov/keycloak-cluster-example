FROM jboss/keycloak-ha-postgres:4.1.0.Final
ADD host-slave.xml /opt/jboss/keycloak/domain/configuration/host-slave.xml
ADD docker-entrypoint.sh /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh", "-b", "0.0.0.0", "--host-config", "host-slave.xml", "-Djboss.domain.master.address=keycloak-master", "-Djboss.node.name=slave01"]
