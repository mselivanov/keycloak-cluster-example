FROM jboss/keycloak:4.1.0.Final
# ADD domain.xml /opt/jboss/keycloak/domain/configuration/domain.xml
# ADD host-master.xml /opt/jboss/keycloak/domain/configuration/host-master.xml
ENTRYPOINT ["/opt/jboss/keycloak/bin/domain.sh", "--host-config=host-master.xml"]
