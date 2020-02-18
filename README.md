# dev
The main repo for the dev-finder project Backend system.

Dev Finder is a platform where aspiring developers can go to find other people to build software projects with.

The backend service consists of two microservices: dev-user and dev-team.
- https://github.com/ckbball/dev-team
- https://github.com/ckbball/dev-user

It is exposed through a REST API.
- https://github.com/ckbball/dev-edge

Dev-user is built with Go, Protobufs, and gRPC for the application code and MongoDB for storage. It also exposes a REST API using grpc-gateway allowing web clients to make api calls to a gRPC server. The project can be built and ran locally using `docker-compose up` and the API can be accessed at http://localhost:8080. User authentication is achieved through Json Web Tokens.

Dev-team is built with Go, Protobufs and gRPC for the application code and MySQL for storage. The service methods can only accessed by the REST API exposed by the edge server. The project can be built and ran locally using `docker-compose up` and the API can be accessed at http://localhost:8082.

Dev-edge is built with Go and the standard library and exposes a REST API over http. The project can be built and ran locally using `docker-compose up` and the API can be accessed at http://localhost:3000.

The project is currently an MVP.
