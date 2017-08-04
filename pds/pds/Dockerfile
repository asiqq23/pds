FROM microsoft/dotnet:1.1-sdk
WORKDIR /home/hackathon/pds/pds/pds


# copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# copy and build everything else
COPY . ./
RUN dotnet publish -c Release -o out

ENV ASPNETCORE_URLS http://*:5000
EXPOSE 5000

ENTRYPOINT ["dotnet", "out/pds.dll"]
