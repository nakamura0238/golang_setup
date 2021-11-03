FROM golang:buster

RUN apt-get upgrade

# 環境変数の設定 $GOPATH/srcをpathに設定
ENV WORK_ROOT /go/src
ENV GO111MODULE=on

# ワーキングディレクトリの設定 環境変数で参照
WORKDIR $WORK_ROOT

COPY ./src .

# パッケージ
RUN go get -u github.com/cosmtrek/air &&\
    go get -u github.com/gin-gonic/gin &&\
    go get -u github.com/jinzhu/gorm

# 設定ファイル読み込み
CMD ["air", "-c", ".air.toml"]
