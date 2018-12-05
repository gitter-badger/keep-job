# Dockerfile for keep-job-portal
# Build with:
# docker build -t keep-job-portal .
# Run with:
# docker run -p 8080:8080 -d -v /tmp/logs:/data/logs --name keep-job-portal keep-job-portal

FROM openjdk:8-jre-alpine
MAINTAINER zhangxuexiang <13811785355@163.com>

ENV VERSION 1.0-SNAPSHOT

RUN echo "http://mirrors.aliyun.com/alpine/v3.8/main" > /etc/apk/repositories \
    && echo "http://mirrors.aliyun.com/alpine/v3.8/community" >> /etc/apk/repositories \
    && apk update upgrade \
    && apk add --no-cache procps unzip curl bash tzdata \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo "Asia/Shanghai" > /etc/timezone

ADD keep-job-portal-${VERSION}.zip /keep-job-portal/keep-job-portal-${VERSION}.zip

RUN unzip /keep-job-portal/keep-job-portal-${VERSION}.zip -d /keep-job-portal \
    && rm -rf /keep-job-portal/keep-job-portal-${VERSION}.zip \
    && sed -i '$d' /keep-job-portal/scripts/startup.sh \
    && echo "tail -f /dev/null" >> /keep-job-portal/scripts/startup.sh

EXPOSE 8080

CMD ["/keep-job-portal/scripts/startup.sh"]
