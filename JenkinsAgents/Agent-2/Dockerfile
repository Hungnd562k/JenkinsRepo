FROM jenkins/ssh-agent:alpine-jdk21

# Chuyen sang user root de cai dat phan mem he thong
USER root

# 1. Cai dat docker-cli
RUN apk add --no-cache docker-cli

# 2. Tao group docker voi GID 986 (trung voi GID cua may host)
RUN addgroup -g 986 docker

# 3. Them user jenkins vao group docker de co quyen doc file socket
RUN adduser jenkins docker

# Chuyen lai ve user jenkins de dam bao an toan bao mat khi chay agent
USER jenkins