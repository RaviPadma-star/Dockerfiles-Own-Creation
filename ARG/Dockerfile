ARG VERSION
FROM almalinux:${VERSION:-8}
ARG Greeting="Hello welcome to Kubernates"
ENV Greet=${Greeting}
RUN echo "$Greeting"
RUN echo "$VERSION"