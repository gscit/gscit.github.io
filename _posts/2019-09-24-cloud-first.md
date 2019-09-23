---
layout: post
title: Cloud Computing 과제 진행방법
<!-- bigimg: /img/path.jpg -->
tags: [cloud, computing]
---

설치는 Pseudo-Distributed Operation 따라서 했다 치고
https://hadoop.apache.org/docs/r3.2.0/hadoop-project-dist/hadoop-common/SingleCluster.html#Pseudo-Distributed_Operation

Wordcount Source 
https://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html#Example:_WordCount_v1.0

java는 openjdk를 받으시면 됩니다. 
https://jdk.java.net/13/ 에서 linux용 tar.gz를 받습니다.
https://download.java.net/java/GA/jdk13/5b8a42f3905b406298b72d750b6919f6/33/GPL/openjdk-13_linux-x64_bin.tar.gz

linux머신에서 직접 받으시든... 윈도우즈에서 옮기시든...  옮긴다음에
옮긴 폴더(디렉토리)내에서 

> tar -xzvf ./openjdk-13_linux-x64_bin.tar.gz 

하면 jdk13폴더가 생깁니다. 리눅스에서는 ls라는 명령어로 디렉토리내 파일 조회가 가능합니다.  
> ls 

그럼 ~/.bashrc 을 여시고  
> nano ~/.bashrc 

맨 밑에  
export JAVA_HOME=/home/ubuntu/jdk-13  
export PATH=${JAVA_HOME}/bin:${PATH}  
export HADOOP_CLASSPATH=${JAVA_HOME}/lib/tools.jar  
이런식으로 jdk-13 폴더에 맞춰서 JAVA_HOME을 설정해주면 됩니다.

그다음엔 임의의 input 폴더를 만듭니다.
> mkdir input && cd input 

다음 가상의 input파일을 만듭니다.
> nano file01

하면 편집기가 나올텐데 거기서 웹사이트에 있는것 처럼 Hello World Bye World 라고 입력하고 Ctrl+x 를 누릅니다. Y를 눌러야 저장이 됩니다.
마찬가지로
> nano file02 

Hello Hadoop Goodbye Hadoop
라고 입력해줍니다. 








