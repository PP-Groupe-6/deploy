FROM golang AS builder
WORKDIR /tmp/
RUN git clone https://github.com/PP-Groupe-6/invoice-microservice && \
    cd invoice-microservice && \
    env CGO_ENABLED=0 GOOS=linux go build 

FROM scratch
COPY --from=builder /tmp/invoice-microservice/invoice-microservice /tmp/
WORKDIR /tmp/
EXPOSE 8002
ENTRYPOINT ["./invoice-microservice"]
