# Servidor con balance de carga

#Fork
$ npm run dev
#Cluster
$ npm run dev-cluster

#Pruebas con pm2
$ pm2 start index.js --name="Servidor1" --watch -- --puerto=8080
$ pm2 start index.js --name="Servidor2" --watch -i max -- --puerto=8089

#Detener pruebas con pm2
$ pm2 stop Servidor1
$ pm2 stop Servidor2

# Nginx

#### Primera parte de la consigna:

$ pm2 start index.js --name="ServidorCluster" --watch -- --puerto=8081 --modo=cluster
$ pm2 start index.js --name="ServidorSimple" --watch -- --puerto=8080

# Finalizar:

$ pm2 stop ServidorCluster
$ pm2 stop ServidorSimple

#### Segunda parte de la consigna:

-   Comentar primer parte del archivo nginx.conf, esta senalado la parte para comentar.
-   Descomentar segunda parte del archivo nginx.conf, esta senalado la parte para descomentar.

$ pm2 start index.js --name="ServidorSimple" --watch -- --puerto=8080

# Finalizar:

$ pm2 stop ServidorSimple
