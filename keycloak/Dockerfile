FROM quay.io/keycloak/keycloak:21.0.1

# ENV KEYCLOAK_ADMIN=admin # Env variable in render
# ENV KEYCLOAK_ADMIN_PASSWORD=admin # Env variable in render

RUN /opt/keycloak/bin/kc.sh build

EXPOSE 8080

ENTRYPOINT ["/opt/keycloak/bin/kc.sh", "start-dev", "--hostname=keycloak-provider.onrender.com", "--hostname-strict=false", "--proxy=edge"]