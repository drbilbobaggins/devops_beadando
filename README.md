# DevOps beadandó – Hello világ alkalmazás

Kerepesy Krisztián - C1QELW
GDE, mérnökinformatikus távoktatás, DEVOPS

Ez a projekt egy egyszerű Node.js + Express alapú „Hello világ” alkalmazás,
amelyet a DevOps tárgy beadandójához készítettem.

Az alkalmazás HTTP-n keresztül érhető el, és egy egyszerű szöveges választ ad.

# Követelmények

A projekt futtatásához szükséges:

- Node.js 
- npm 

# Helyi build és futtatás

Klónozza vagy töltse le a repót a következő elérhetőségről:
https://github.com/drbilbobaggins/devops_beadando.git

Ezután:
npm install
npm start

Böngészőben megnyitható: http://localhost:8080

# Docker használata

Az alkalmazás Docker konténerben is futtatható:

A projekt gyökerében kell futtatni:
docker build -t devops_beadando:latest
docker run -p 8080:8080 devops_beadando:latest

Utána elérhető ugyanitt:
http://localhost:8080

# CI pipeline és Docker Hub image

A GitHub Actions CI pipeline minden `master` branchre történő push után automatikusan:

1. lefuttatja az `npm install` lépést,
2. felépíti a Docker image-et a projekt Dockerfile-ja alapján,
3. feltölti az image-et a Docker Hubra.

Az image a Docker Hubon található, itt: `mrbaggins/devops_beadando:latest`
(teljes eléréssel: https://hub.docker.com/repository/docker/mrbaggins/devops_beadando/general)

Image lehúzása és futtatása a Docker Hubról:

docker pull mrbaggins/devops_beadando:latest
docker run -p 8080:8080 mrbaggins/devops_beadando:latest