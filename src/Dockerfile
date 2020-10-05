#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM mcr.microsoft.com/dotnet/core/sdk:3.1
ENV VlingoVersion=0.8.2
WORKDIR /src
COPY . .
RUN dotnet restore "Vlingo.Directory.Tests/Vlingo.Directory.Tests.csproj"
RUN dotnet build "Vlingo.Directory.Tests/Vlingo.Directory.Tests.csproj"
ENTRYPOINT ["dotnet", "test", "-v","n"]