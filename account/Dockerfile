FROM golang AS builder
WORKDIR /tmp/
RUN git clone https://github.com/PP-Groupe-6/account-microservice && \
    cd account-microservice && \
    env CGO_ENABLED=0 GOOS=linux go build 

FROM scratch
COPY --from=builder /tmp/account-microservice/account-microservice /tmp/
WORKDIR /tmp/
EXPOSE 8000
ENTRYPOINT ["./account-microservice"]
