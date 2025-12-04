# DevOps beadandó – Hello világ alkalmazás

Kerepesy Krisztián - C1QELW
GDE, mérnökinformatikus távoktatás, DEVOPS

Ez a projekt egy egyszerű Node.js + Express alapú „Hello világ” alkalmazás,
amelyet a DevOps tárgy beadandójához készítettem.

Az alkalmazás HTTP-n keresztül érhető el, és a gyökér útvonalon (`/`) egy egyszerű szöveges választ ad.

---

## Követelmények

A projekt futtatásához szükséges:

- Node.js 
- npm 

## Telepítés és futtatás

1. Klónozza vagy töltse le a repót (GitHubról) a következő elérhetőségről:
https://github.com/drbilbobaggins/devops_beadando.git

2. Függőségek telepítése:

npm install

3. Az alkalmazás indítása:

npm start

Böngészőben megnyitható: http://localhost:8080

## Docker használata

Az alkalmazás Docker konténerben is futtatható.

A projekt gyökerében futtassa:

```bash
docker build -t devops_beadando:latest .

Az image futtatása:

docker run -p 8080:8080 devops_beadando:latest

Utána elérhető ugyanitt:
http://localhost:8080