- Сборка приложения
```bash
./mvnw clean package
```

- Запуск приложения
```bash
./mvnw spring-boot:run
```

- Сборка образа
```bash
docker build --platform -t otus-hw-1-health-check .
```

- Или сборка образа под amd64
```bash
docker build --platform linux/amd64 -t otus-hw-1-health-check .
```

- Указать тэг
```bash
docker tag otus-hw-1-health-check mksikayo/otus-hw-1-health-check
```

- Запушить образ на dockerhub
```bash
docker push mksikayo/otus-hw-1-health-check
```

- Запустить образ
```bash
docker run -p8000:8000 mksikayo/otus-hw-1-health-check
```

- Проверить endpoint /health
```bash
curl http://127.0.0.1:8000/health
```
