# dev
The main repo for the dev-finder project Backend system.

Dev Finder is a web site where aspiring developers can go to find other people to build software projects with.

The backend service consists of two microservices: dev-user and dev-team.
https://github.com/ckbball/dev-team
https://github.com/ckbball/dev-user

It is exposed through an edge server.
https://github.com/ckbball/dev-edge

Dev-user is built with Golang, Protobufs, and gRPC for the application code and MongoDB for storage. It also exposes a REST API using grpc-gateway allowing web clients to make api calls to a gRPC server. The project can be built and ran using docker-compose up and the API can be accessed at http://localhost:8080.

Dev-team is build with Golang, Protobufs and gRPC for the application code and MySQL for storage. A REST API is exposed through the grpc-gateway attached to the gRPC server allowing web clients to make api calls. The project can be built and ran using docker-compose up and the API can be accessed at http://localhost:8082.

The project is currently an MVP.
