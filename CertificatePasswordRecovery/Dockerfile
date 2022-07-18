FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /app

COPY  ./
WORKDIR /app/handbook

RUN dotnet publish

EXPOSE 5051

#FROM mcr.microsoft.com/dotnet/runtime:6.0
# WORKDIR /app/handbook/rc/HB.Api/bin/Debug/net6.0/publish


# ENTRYPOINT ["dotnet", "HB.Api.dll", "--urls=http://0.0.0.0:5051"]