
##Mini Server con semaforos.

JorgeDuranChinchilla C02679 KennethFabricioDelgadoCardenas C22540

Intrucciones para correr la tc4 server producer-consumer con semaforos

Abrir dos terminales, en una de ellas el servidor:

gcc -D_POSIX_C_SOURCE=200809L -std=c11 -Wall -Wextra -Wpedantic -O2 -pthread -Iincludes \
  src/server_procon.c src/net_utli.c -o server_procon

Y luego:

./server_procon 8080 4


luego en la otra terminal correr los clientes: .gcc -std=c11 -Wall -Wextra -Wpedantic -O2 -pthread -Iincludes \
  src/load_client.c -o load_client
  
  y luego time ./load_client 127.0.0.1 8080 4 150

Ctrl + c para terminar
