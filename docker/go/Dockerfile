FROM golang:alpine AS builder

WORKDIR /go/src

COPY /src/hello /go/src

RUN go mod init dornelespires/hello && \
    go build

FROM scratch

COPY --from=builder /go/src /

CMD [ "./hello" ]