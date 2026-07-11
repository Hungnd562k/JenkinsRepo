FROM jenkins/ssh-agent:alpine-jdk21

# stat -c '%g' /var/run/docker.sock
# Chạy lệnh trên để kiểm tra GID của nhóm docker sau đó thay vào biến DOCKER_GID
ARG DOCKER_GID=986

USER root
RUN apk add --no-cache docker-cli

# Tạo group docker với GID tương ứng và thêm user jenkins vào group đó
RUN addgroup -g ${DOCKER_GID} docker && \
    addgroup jenkins docker

USER jenkins