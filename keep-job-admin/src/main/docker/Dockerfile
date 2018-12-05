# Dockerfile for keep-job-admin
# Build with:
# docker build -t keep-job-admin .
# Run with:
# docker run -p 8090:8090 -d -v /tmp/logs:/data/logs --name keep-job-admin keep-job-admin

FROM openjdk:8-jre-alpine
MAINTAINER zhangxuexiang <13811785355@163.com>

ENV VERSION 1.0-SNAPSHOT

RUN echo "http://mirrors.aliyun.com/alpine/v3.8/main" > /etc/apk/repositories \
    && echo "http://mirrors.aliyun.com/alpine/v3.8/community" >> /etc/apk/repositories \
    && apk update upgrade \
    && apk add --no-cache procps unzip curl bash tzdata \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo "Asia/Shanghai" > /etc/timezone

ADD keep-job-admin-${VERSION}.zip /keep-job-admin/keep-job-admin-${VERSION}.zip

RUN unzip /keep-job-admin/keep-job-admin-${VERSION}.zip -d /keep-job-admin \
    && rm -rf /keep-job-admin/keep-job-admin-${VERSION}.zip \
    && sed -i '$d' /keep-job-admin/scripts/startup.sh \
    && echo "tail -f /dev/null" >> /keep-job-admin/scripts/startup.sh

EXPOSE 8090

CMD ["/keep-job-admin/scripts/startup.sh"]
