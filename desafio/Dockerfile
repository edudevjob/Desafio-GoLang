# Init image base golang:alpine
FROM golang:alpine AS builder

WORKDIR /src

COPY . .

RUN go build -ldflags '-s -w' main.go

FROM scratch

WORKDIR /

COPY --from=builder /src / 

CMD ["./main"]


# ❯ docker run -p 8080:8080 eduardotecnologo/desafio                                                                    ─╯
# Fullcycle Rocks!
# REPOSITORY                       TAG       IMAGE ID       CREATED            SIZE
# eduardotecnologo/desafio         latest    f6f10c675984   About a minute ago 1.23MB*