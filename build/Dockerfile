# goバージョン
FROM golang:1.20.4-alpine
# アップデートとgitのインストール
RUN apk update && apk add git
# boiler-plateディレクトリの作成
RUN mkdir /go/src/boiler-plate
# ワーキングディレクトリの設定
WORKDIR /go/src/boiler-plate

RUN go mod init go-docker-sample
RUN go mod tidy

# ホストのファイルをコンテナの作業ディレクトリに移行
ADD . /go/src/boiler-plate
# パッケージのインポート
RUN go get -u golang.org/x/tools/cmd/goimports