FROM microsoft/dotnet:1.0.0-preview2-sdk

RUN mkdir /app
WORKDIR /app

COPY project.json /app
RUN ["dotnet", "restore"]

COPY . /app
RUN ["dotnet", "build"]

ENV ASPNETCORE_SERVER.URLS http://*:5000
EXPOSE 5000
CMD ["dotnet", "run"]