FROM golang AS builder
WORKDIR /tmp/
RUN git clone https://github.com/PP-Groupe-6/transfer-microservice && \
    cd transfer-microservice && \
    env CGO_ENABLED=0 GOOS=linux go build 

FROM scratch
COPY --from=builder /tmp/transfer-microservice/transfer-microservice /tmp/
WORKDIR /tmp/
EXPOSE 8001
ENTRYPOINT ["./transfer-microservice"]
