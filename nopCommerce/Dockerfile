FROM mcr.microsoft.com/dotnet/sdk:8.0
LABEL author="anitha"
LABEL project="nop"
#Installing unzip
RUN apt update
RUN apt install unzip -y
RUN mkdir /app
WORKDIR /app
ARG DOWNLOAD_URL="https://github.com/nopSolutions/nopCommerce/releases/download/release-4.70.4/nopCommerce_4.70.4_NoSource_linux_x64.zip" 
#Downloading a file from internet
ADD ${DOWNLOAD_URL} /app/
EXPOSE 5000
#Unzip the file and bin and logs folder
RUN unzip nopCommerce_4.70.4_NoSource_linux_x64.zip
RUN mkdir bin && mkdir logs
CMD ["dotnet","Nop.Web.dll","--url","http://0.0.0.0:5000"]
