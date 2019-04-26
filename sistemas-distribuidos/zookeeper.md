# ZooKeeper

Nodos persistentes: ese nodo esta grabado en la base de datos distribuidas y por mas que el cliente se desconecte, sigue grabado

Nodos efimeros: solo se mantienen en la estructura mientras siga conectado y vivo a ZooKeeper. Si deja de mandar latidos, ese nodo y todos los nodos efimeros que creo, se borran de la estructura.

Elección de master: se escribe en un archivo secuencialmente y zookeeper asigna un numero a cada nodo. El nodo con el menor numero es el master. Cada nodo vuelve a leer el archivo para ver que numero le toco. Si se quiere que al morirse el master se elija otro, debe ser un nodo efimero.

Todos los demás nodos se subscriben para escuchar la muerte del master y cuando reciba el evento, vuelve a chequear el archivo para saber si es el master. Si es el master se registra como master, sino se subscribe al master.