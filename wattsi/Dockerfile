FROM debian:sid

RUN apt-get update && \
    apt-get install -y curl binutils git && \
    curl ftp://freepascal.stack.nl/pub/fpc/beta/3.0.0-rc1/x86_64-linux/fpc-3.0.0rc1.x86_64-linux.tar > fpc-3.0.0rc1.x86_64-linux.tar && \
    tar vxf fpc-3.0.0rc1.x86_64-linux.tar && \
    cd fpc-3.0.0rc1.x86_64-linux && \
    ./install.sh && \
    cd / && \
    git clone https://github.com/whatwg/wattsi && \
    cd wattsi && \
    ./build.sh && \
    cp bin/wattsi /bin/ && \
    cd / && \
    rm -fr fpc-3.0.0rc1.x86_64-linux.tar fpc-3.0.0rc1.x86_64-linux wattsi && \
    rm -rf /var/lib/apt/lists/*
