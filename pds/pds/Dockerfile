FROM microsoft/dotnet:1.1-sdk
WORKDIR /home/hackathon/checkout/checkout/checkout

# copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# copy and build everything else
COPY . ./
RUN dotnet publish -c Release -o out
ENTRYPOINT ["dotnet", "out/dotnetapp.dll"]