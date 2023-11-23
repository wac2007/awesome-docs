# Why not using spotify/mkdocs directly?
# https://backstage.io/docs/features/techdocs/how-to-guides/#how-to-add-mermaid-support-in-techdocs

FROM python:3.10-alpine

RUN apk update && apk --no-cache add gcc musl-dev openjdk11-jdk curl graphviz ttf-dejavu fontconfig

RUN pip install --upgrade pip && pip install mkdocs-techdocs-core==1.3.2

# Adding mermaid support
RUN pip install mkdocs-kroki-plugin==0.7.0
# RUN pip install markdown-inline-mermaid

# Create script to call plantuml.jar from a location in path
RUN echo $'#!/bin/sh\n\njava -jar '/opt/plantuml.jar' ${@}' >> /usr/local/bin/plantuml
RUN chmod 755 /usr/local/bin/plantuml

ENTRYPOINT [ "mkdocs" ]
