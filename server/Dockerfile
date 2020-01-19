FROM rust:stretch

RUN cargo install diesel_cli --no-default-features --features postgres \
  && ln -snf /usr/share/zoneinfo/Asia/Ulaanbaatar /etc/localtime \
  && echo "Asia/Ulaanbaatar" > /etc/timezone

WORKDIR /usr/src/app

EXPOSE 3001
