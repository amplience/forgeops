FROM gcr.io/forgerock-io/ds-empty/pit1:7.0.0-25acac1436304ec9a357fcd1a3ef5c8fb765415d
USER root
RUN chown -R forgerock:root /opt/opendj
USER forgerock
COPY --chown=forgerock:root cts /opt/opendj/
COPY --chown=forgerock:root scripts /opt/opendj/scripts
ARG profile_version
RUN bin/setup.sh "$profile_version"  && rm bin/setup.sh