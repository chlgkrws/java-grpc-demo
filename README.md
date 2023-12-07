# java-grpc-demo

## 프로젝트 설명 / 목적
이 프로젝트는 Java로 작성된 간단한 GRPC 서버를 구축하는 방법을 설명합니다. 서버는 성과 이름을 입력 받아 인사말을 응답합니다.

(Java 언어로 GRPC Server 및 Client(Stub)를 구축하여 gRPC의 기본구조 이해)

## 실행
### 1. Proto 컴파일
```shell
gradle
other > generateProto

또는 

https://github.com/grpc/grpc-java/tree/master/compiler 컴파일러 설치 후 
protoc --plugin=protoc-gen-grpc-java=$PATH_TO_PLUGIN -I=$SRC_DIR 
  --java_out=$DST_DIR --grpc-java_out=$DST_DIR $SRC_DIR/HelloService.proto
```
### 2. GRPC 서버 실행
GrpcServer 클래스에서 GRPC 서버를 구동합니다. 서버는 클라이언트의 요청을 수신하고 처리합니다.


![img.png](https://github.com/chlgkrws/java-grpc-demo/blob/main/github/img.png)

### 3. GRPC 클라이언트 실행
GrpcClient 클래스를 사용하여 서버에 요청을 보내고 응답을 받습니다.

## Reference

https://grpc.io/docs/languages/java/quickstart

https://www.baeldung.com/grpc-introduction

https://minddong.tistory.com/71
