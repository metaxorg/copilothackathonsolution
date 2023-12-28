# 构建 Quarkus 本机镜像

## 构建本机可执行文件

```bash
mvn clean package -Pnative
```

## 使用 Dockerfile.native-micro 构建 docker 镜像

```bash
docker build -f Dockerfile.native-micro -t quarkus/quarkus-native-micro .
```

## 运行 docker 镜像

```bash
docker run -i --rm -p 8080:8080 quarkus/quarkus-native-micro
```

## 测试应用程序

```bash
curl -v http://localhost:8080/hello
```