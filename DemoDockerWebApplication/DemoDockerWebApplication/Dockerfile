FROM microsoft/aspnetcore:2.0 AS base
WORKDIR /app
EXPOSE 80

#FROM microsoft/aspnetcore-build:2.0 AS build
FROM microsoft/dotnet:2.1-sdk AS build
WORKDIR /src
COPY DemoDockerWebApplication.csproj .
RUN dotnet restore DemoDockerWebApplication.csproj
COPY . .
WORKDIR /src
RUN dotnet build DemoDockerWebApplication.csproj -c Release -o /app

FROM build AS publish
RUN dotnet publish DemoDockerWebApplication.csproj -c Release -o /app

FROM microsoft/dotnet:2.1-aspnetcore-runtime AS runtime
WORKDIR /app
COPY --from=publish /app .
ENTRYPOINT ["dotnet", "DemoDockerWebApplication.dll"]
EXPOSE 80

