# Spring PetClinic Sample Application

## ローカル環境での実行方法

JDK 17 以上をインストールし、project 内に同梱されている Maven にてビルド、実行ができます。

```bash
git clone https://github.com/spring-projects/spring-petclinic.git
cd spring-petclinic
./mvnw package -DskipTests
java -jar target/*.jar
```

実行後は http://localhost:8080/ にて動作確認ができます。

<img width="1042" alt="petclinic-screenshot" src="https://cloud.githubusercontent.com/assets/838318/19727082/2aee6d6c-9b8e-11e6-81fe-e889a5ddfded.png">

また、Spring Boot のプラグインで実行すれば、ソースコードの修正が再起動せずに反映されます。

```bash
./mvnw spring-boot:run
```

## CI 環境のセットアップ

ローカル環境にて、CI 環境を実行したい場合は、以下の方法でできます。

```bash
docker compose -f ci/compose.yaml up -d
```

## Docker コンテナのビルド

Docker イメージを作成したい場合は、以下のコマンドで可能です。

```bash
./mvnw spring-boot:build-image
```
