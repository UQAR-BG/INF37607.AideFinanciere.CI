FROM mcr.microsoft.com/dotnet/sdk:8.0

WORKDIR /app

EXPOSE 80
EXPOSE 443

RUN dotnet dev-certs https --clean
RUN dotnet dev-certs https -t

ENTRYPOINT [ "dotnet", "watch", "--project", "INF37607.AideFinanciere.WebAPI", "run", "--urls", "https://*:443" ]