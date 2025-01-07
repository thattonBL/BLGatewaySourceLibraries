This is the dev project that contains the parent solution for running BLGateway Microservices in Docker.

![Gateway drawio](https://github.com/thattonBL/BLGatewaySourceLibraries/assets/79150422/9e1f25c2-766e-489c-97a2-9fe0eef83c4d)

Once checked out you will see something like the following:

![New-Checkout](https://github.com/user-attachments/assets/4475c1c6-9903-4e26-aea3-b2811648e96a)

Then within the folder structure that you have downloaded checkout each project into its associated root folder. You will need to edit the path it checks out too, to ensure that directories aren not duplicated needlessly. For clarity the .git and .sln file should sit directly within the project named directory not within a sub directory of the same name.

This solution is set up with the docker-compose file to contain all the necessary directories and sql intialisation scripts. So when the complete suite of microservice are checked out then the whole system should work out of the box.
(update 07/01/25) The shared libraries are now nuget packages run the following command, to add the BL package source, before you do a build on the checkout solution:
```
dotnet nuget add source -n Gateway_Nuget_Feed https://pkgs.dev.azure.com/BritishLibrary-AppDev/Gateway/_packaging/Gateway_Nuget_Feed/nuget/v3/index.json
```
The Microservice projects should then build, if you want to work on the shared libraries simply remove the link to the nuget packaged code and link to the library project instead.
If you make changes to any of the libraries you will have to commit those changes, test the updated nuget package and commit with the updated nuget package reference.

Each Microservice has its own .sln file and docker-compose to allow it to run with it dependencies in isolation also if you do not need to run the entire application suite.

Note: IF you are running the full system and wanting to see messages coming through in the UI please use the https ports.
