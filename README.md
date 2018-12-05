# keep-job

KEEP-JOB 是一个轻量级分布式任务调度平台，其核心设计目标是开发迅速、学习简单、轻量级、易扩展。现已开放源代码并接入多家公司线上产品线，开箱即用。

能够集中化管理应用不同环境、不同集群的任务，任务修改后能够实时生效，并且具备规范的权限、流程治理等特性，适用于微服务任务管理场景。

调度中心服务端基于Spring Boot和Spring Cloud开发，打包后可以直接运行，不需要额外安装Tomcat等应用容器。

Java客户端不依赖任何框架，能够运行于所有Java运行时环境，同时对Spring/Spring Boot环境也有较好的支持。

[![Build Status](https://travis-ci.org/zhangxuexiang/keep-job.svg?branch=master)](https://travis-ci.org/zhangxuexiang/keep-job)
<a href="https://hub.docker.com/r/com.keep/keep-job/">
    <img src="https://img.shields.io/badge/docker-passing-brightgreen.svg" />
</a>
[![GitHub release](https://img.shields.io/github/release/zhangxuexiang/keep-job.svg)](https://github.com/zhangxuexiang/keep-job/releases)
[![Maven Central Repo](https://img.shields.io/maven-central/v/com.keep/keep-job.svg)](https://mvnrepository.com/artifact/com.keep/keep-job)
[![Coverage Status](https://coveralls.io/repos/github/zhangxuexiang/keep-job/badge.svg?branch=master)](https://coveralls.io/github/zhangxuexiang/keep-job?branch=master)
<a href="https://scan.coverity.com/projects/zhangxuexiang-keep-job">
  <img alt="Coverity Scan Build Status" src="https://scan.coverity.com/projects/17364/badge.svg" />
</a>
[![codecov](https://codecov.io/gh/zhangxuexiang/keep-job/branch/master/graph/badge.svg)](https://codecov.io/gh/zhangxuexiang/keep-job)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
