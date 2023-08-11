FROM cloudsuite/java:openjdk11
ENV FABAN_USER faban
ENV FABAN_VERSION 1.4
RUN apt-get update -y \
	&& apt-get install -y --no-install-recommends telnet wget tar curl \
	&& rm -rf /var/lib/apt/lists/* \
	&& groupadd -r $FABAN_USER  \
	&& useradd -r -g $FABAN_USER $FABAN_USER

ENV BASE_PATH /usr/src
ENV FABAN_HOME $BASE_PATH/faban
ENV FABAN_OUTPUT_DIR $BASE_PATH/outputFaban

RUN cd $BASE_PATH \
	&& wget "http://10.30.1.18:8080/datasets/cloudsuite/faban-kit-$FABAN_VERSION.tar.gz" \
	&& tar -xzf faban-kit-$FABAN_VERSION.tar.gz

ENV FABAN_USER faban
