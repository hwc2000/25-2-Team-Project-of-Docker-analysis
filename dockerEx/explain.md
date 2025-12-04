# 시연 보고서

---

## 개요 
1. Topology
2. 도커의 설치 과정 
3. 도커 허브 사용
4. 간단한 실험 예제

---
## Topology
### 1. Server VM (Linux)
![alt text](image-2.png)
---
### 2. Client OS (Windows)
![alt text](image.png)
---

## 도커의 설치 과정
1. 저장소 업데이트 후 도커 다운

```
sudo apt update
sudo apt install -y docker.io
```
![alt text](image-1.png)

y/n 이 뜨는데 y를 입력하면 설치 됩니다.

```
docker --version
```
![alt text](image-3.png)  

으로 잘 설치되었는지 확인합니다.

---
2. 사용자 등록

![alt text](image-4.png)

sudo같은 별도의 권한 없이는 다음과 같이 도커 데몬의 접근이 막힌다. 그래서 현재 사용자를 도커 사용자 그룹에 추가 해 줘야 한다.
```
sudo usermod -aG docker $USER
```
![alt text](image-5.png)

시스템 리부트 하거나 newgrp docker 등을 통해 초기화 시켜주면 다음과 같이 적용 된다.

3. 컨테이너 테스트 


