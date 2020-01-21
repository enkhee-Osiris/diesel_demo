FROM rust:stretch

RUN cargo install diesel_cli --no-default-features --features postgres \
  && cargo install cargo-watch \
  && ln -snf /usr/share/zoneinfo/Asia/Ulaanbaatar /etc/localtime \
  && echo "Asia/Ulaanbaatar" > /etc/timezone

WORKDIR /usr/src/app

COPY Cargo.* ./

RUN mkdir -p ./src && echo -n "fn main() {\n    println!(\"Hello World);\n}" > ./src/main.rs && cargo fetch

COPY . .

EXPOSE 3001

CMD ["cargo", "run"]
