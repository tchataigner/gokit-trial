FROM golang

RUN mkdir -p /go/src/github.com/tchataigner/gokit-trial

ADD . /go/src/github.com/tchataigner/gokit-trial

RUN go get  -t -v ./...
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/tchataigner/gokit-trial/notificator/cmd  -watch github.com/tchataigner/gokit-trial/notificator
