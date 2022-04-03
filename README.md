# ac-mod-directory
Mod directory web apps


## Project structure
[Example project structure](https://github.com/golang-standards/project-layout)

```
github.com/user/some_project/
├── pkg/ (common own-created packages for all services )
|   ├── errors/
|   ├── log/
|   ├── metrics/
|   ├── sd/
|   |   ├── consul/
|   |   └── kubernetes/
|   └── tracing/
├── internal/ (internal packages)
|   ├── somelib/
├── services/
|   ├── account/
|   |   ├── pb/
|   |   |   ├── account.proto
|   |   |   └── account.pb.go
|   |   ├── handler.go
|   |   ├── main.go
|   |   ├── main_test.go
|   |   ├── Dockerfile
|   |   └── README.md
|   ├── auth/
|   ├── frontend/
|   └── user/
├── vendor/ (common vendor-packages for all services)
├── docker-compose.yml
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

[Another approach](https://www.dudley.codes/posts/2020.05.19-golang-structure-web-servers/)
```
├── app/
|   └── service-api/**
├── cmd/
|   └── service-tool-x/
├── internal/
|   └── service/
|       └── mock/
├── pkg/
|   ├── client/
|   └── dtos/
├── (.editorconfig, .gitattributes, .gitignore)
└── go.mod
```

Service structure

```
└── service-api/
    ├── cfg/
    ├── middleware/
    ├── routes/
    |   ├── makes/
    |   |   └── models/**
    |   ├── create.go
    |   ├── create_test.go
    |   ├── get.go
    |   └── get_test.go
    ├── webserver/
    ├── main.go
    └── pipeline.go
```