This is the dev project that contains the parent solution for running BLGateway Microservices in Docker.
Once checked out you can add the Microservices you want to work on by simply checking them out to the src -> Microservices directory found within this solution.
This solution is set up with the docker-compose file to contain all the necessary directories and sql intialisation scripts. So when the complete suite of microservice are checked out to the src -> Microservices directory then the whole system should work out of the box.
A complete solution (as it stand now 6/6/24) currently looks like:

![Parent-Project](https://github.com/thattonBL/BLGatewaySourceLibraries/assets/79150422/2dcfef25-c896-492e-84b8-b6eb0c74513b)

With the directory structure looking ike this, see to the right:

![Parent-Solution-FileStructure](https://github.com/thattonBL/BLGatewaySourceLibraries/assets/79150422/2aef5806-6c78-48ab-b446-f6fe96f80820)

Each microservice still has its own .sln file and can be worked on indidually. They're setup by default to sit within the above structure as the generic library dependencies are pulled in from the parent solution.
So an individual Microservice looks like this, with the src -> BuildingBlocks and the src -> Common directories just as solution folders not actually directories and pulling in the libraries contained therein from the parent project:

![Child-Solution-Explorer](https://github.com/thattonBL/BLGatewaySourceLibraries/assets/79150422/0b8111b3-9d6a-4eb8-bce5-d4f49b5dd508)

The directory structure looking like this:

![Child-Solution-FileStructure](https://github.com/thattonBL/BLGatewaySourceLibraries/assets/79150422/72cf6a6c-5ddf-4d5f-8e0e-9e53b5672924)
