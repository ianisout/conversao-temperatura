FROM node:14.17.5
#workdir whatever name you want
WORKDIR /app-docker
# * means all files, both package and package-lock
COPY ./package*.json ./
RUN npm install
# copy everything else other than the package.json stuff
# utilizando o uso de CAMADAS, ganha tempo, ganha desempenho no cache utilizar camadas
COPY . .
EXPOSE 8080
# CMD só será executado quando executar container
CMD ["node", "server.js"]

# go run $docker image build -t ianisout/conversao-temperatura:v1 .
# GOGOGO