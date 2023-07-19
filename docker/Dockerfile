FROM public.ecr.aws/p6e8q1z1/aleph-node:r-11.3

RUN apt update && \
        apt install google-perftools binutils -y && \
        apt clean && \
        rm -rf /var/lib/apt/lists/*

COPY docker/docker_entrypoint.sh /node/docker_entrypoint.sh
RUN chmod +x /node/docker_entrypoint.sh

ENTRYPOINT ["./docker_entrypoint.sh"]