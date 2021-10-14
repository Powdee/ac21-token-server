# actix-rust-OAuth

Rust has picked up a lot of momentum since we last looked at it in 2015. Companies like Amazon and Microsoft have adopted it for a growing number of use cases. Microsoft, for example, sponsors the Actix project on GitHub, which is a general purpose open source actor framework based on Rust. The Actix project also maintains a RESTful API development framework, which is widely regarded as a fast and performant web framework. Although the project was temporarily on hold in early 2020, the project ownership has moved to a new maintainer, and development continues.

I was about to start a new project on Cardano blockchain and we need simple CRUD operations with Database of users and products and create a portal to communicate with Cardano blockchain.
This repo is only for creating CRUD operations with basic OAuth. A little showcase how `Rust` works on `actix-web` framework.

## RESTful API CRUD Operations
* GET /users
* GET /users/{id}
* POST /users
* DELETE /users/{id}

## Setup

First, have PostgreSQL installed and running.

Make sure you have `cargo` installed.

Next, run in the terminal:
```shell
cargo run
```

When `run` has executed successfully, run the API to GET users:
```shell
curl -H "Authorization: Bearer $TOKEN" -v 127.0.0.1:8080/users
```

Or run the API to Create user:
```shell
curl -v -H "Content-Type: application/json; Authorization: Bearer $TOKEN"  -X POST -d '{"first_name": "foo1", "last_name": "bar1", "email": "foo1@bar.com"}' 127.0.0.1:8080/users
```
