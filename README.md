# sns-root-service


## 1. 네트워크 생성

```
docker network create sns-network
```

## 2. 각 서비스 실행

2.1. 루트 서비스 시작
```aiexclude
cd sns-root-service
mkdir -p nginx
# nginx.conf 파일 생성 (위에서 제공한 내용으로)
docker-compose up -d
```

2.2. post 서비스 시작

```aiexclude
cd sns-post-service
docker-compose up -d
```

2.3. like 서비스 시작

```aiexclude
cd sns-like-service
docker-compose up -d
```

## 3. 서비스

- API Gateway를 통한 접근: http://localhost/api/posts, http://localhost/api/likes
- 직접 접근: http://localhost:8081, http://localhost:8082