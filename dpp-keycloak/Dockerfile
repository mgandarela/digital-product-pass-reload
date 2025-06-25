# Dockerfile para Keycloak con curl (basado en RHEL)
FROM quay.io/keycloak/keycloak:latest

# Cambiar a root para instalar paquetes
USER root

# Instalar curl y limpiar metadata
RUN microdnf install -y curl && \
    microdnf clean all && \
    rm -rf /var/cache/yum /var/cache/dnf

# Volver al usuario keycloak (no root)
USER keycloak
