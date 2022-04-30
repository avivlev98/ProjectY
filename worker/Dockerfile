FROM mcr.microsoft.com/dotnet/core/runtime:2.2

WORKDIR /code

ADD src/Worker /code/src/Worker

RUN dotnet restore -v minimal src/Worker \
    && dotnet publish -c Release -o "./" "src/Worker/" 

CMD dotnet src/Worker/Worker.dll
