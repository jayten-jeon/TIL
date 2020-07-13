# Docker 기초

`docker run -d -p 80:80 docker/getting-started`

- `-d`

  contianer를 detached mode로 실행한다 (백그라운드로 실행)

- `-p 80:80`

  Host의 80 포트를  container의 80포트로 mapping

- `Docker/getting-started`

  사용할 image

**꿀팁** 

flag를 조합해서 아래와 같이 사용할 수 있다.

`docker run -dp 80:80 docker/getting-started`


