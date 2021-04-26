FROM euantorano/zig:latest

COPY --from=golang:1.16-alpine /usr/local/go/ /usr/local/go/
 
ENV PATH="/usr/local/go/bin:${PATH}"

WORKDIR /usr/local/bin

ADD zcc-linux zxx-linux zcc-windows zxx-windows /usr/local/bin/

RUN chmod +x zcc-linux zxx-linux zcc-windows zxx-windows

RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh