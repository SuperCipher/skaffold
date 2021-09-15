FROM postgres:13.0

#Add ca-certificate to support the CA for S3
RUN apt update && \
    apt install ca-certificates wget -y && \
    rm -rf /var/lib/apt/lists/*

#Add wal-g from https://github.com/wal-g/wal-g/releases
RUN cd /tmp && \
    wget https://github.com/wal-g/wal-g/releases/download/v0.2.19/wal-g.linux-amd64.tar.gz && \
    tar -zxvf wal-g.linux-amd64.tar.gz && \
    mv wal-g /usr/bin/
