FROM golang as builder

ADD . /go/src/DesafioDocker

RUN go install DesafioDocker

FROM scratch
COPY --from=builder /go/bin/DesafioDocker .
CMD ["/DesafioDocker"]

# ENTRYPOINT /go/bin/DesafioDocker