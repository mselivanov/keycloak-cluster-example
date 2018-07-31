FROM jboss/keycloak-ha-postgres:4.1.0.Final
ADD domain.xml /opt/jboss/keycloak/domain/configuration/domain.xml
ADD host-master.xml /opt/jboss/keycloak/domain/configuration/host-master.xml
ADD docker-entrypoint.sh /docker-entrypoint.sh
RUN /opt/jboss/keycloak/bin/add-user.sh --user admin --password Qazwsx123 --enable
ENTRYPOINT ["/docker-entrypoint.sh", "-b", "0.0.0.0", "--host-config", "host-master.xml", "-Djboss.bind.address=keycloak-master", "-Djboss.bind.address.management=keycloak-master"]
