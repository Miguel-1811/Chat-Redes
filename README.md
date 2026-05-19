## Chat TCP/UDP en Java

> Proyecto final  Redes  Itson

Aplicacion de chat Cliente-Servidor desarollada en java que 
les permitetener una comunicacion en tiempo real mediante
los sockets de TCP y UDP,El sistema cuenta con soporte para mensajes 
grupales y privadas.

---

## Descripcion
El sistema implementa una arquitectura cliente-Servidor donde tienes un servidor
central donde gestiona las conexiones del cual puede ser mediante TCP U UDP
y retransmite mensajes entre los clientes conectados, se utilizan hilos independientes 
para manejar cada cliente de forma concurrente lo cual permite tener varios clientes
conectados simultaneamente y sin bloqueos.

---

## Integrantes
| Nombre | Matricula |
|--------|-----------|
| Alejandra Isabel Figueroa Banda | 262703 |
| Miguel Angel Urias Espinoza     | 244896 |

---

## Tecnologias Utilizadas

- **Java 17+**
- **TCP Sockets** - Conexion confiable orientada a flujo
- **UDP Sockets** - comunicacion sin conexion de baja latencia
- **Multihilos** (`Thread` / `Runnable`) - manejo concurrente de clientes

---

## Estructura del proyecto

```
Aplicacion-Redes
│
├── Source Packages
│   │
│   ├── Cliente
│   │   ├── TCPClient.java
│   │   └── UDPClient.java
│   │
│   ├── Diseño
│   │   ├── Menu_Principal.java
│   │   └── chatDialog.java
│   │
│   ├── Juego
│   │   ├── GamePanel.java
│   │   ├── GuitarHeroGame.java
│   │   ├── Level.java
│   │   ├── MenuPrincipal.java
│   │   ├── Note.java
│   │   │
│   │   └── Niveles
│   │       ├── Level1.java
│   │       ├── Level2.java
│   │       ├── Level3.java
│   │       ├── Level4.java
│   │       ├── LevelData.java
│   │       └── ScoreManager.java
│   │
│   ├── Resources
│   │
│   ├── Server
│   │   ├── TCPServer.java
│   │   └── UDPServer.java
│   │
│   └── TestPackages
│
├── Libraries
│
└── TestLibraries
```

## Diagrama de flujo del sistema 

![Diagrama de flujo](https://github.com/Miguel-1811/Chat-Redes/blob/0f2c335935ba45d58309e75efba6ea7b8adb9090/Resources/Diagrama%20de%20flujo.webp)

---

## Como ejecutar

### Requisitos previos

- Java JDK 17 o superior instalado
- Terminal / Git Bash

### Compilar el proyecto
### Tienes que abrir una terminal dentro de la caroeta donde tengas los jar del proyecto, escribir el siguiente comando
```Bash
java -jar chat.jar
```

### Iniciar el servidor
### para servidor TCP

```Terminal
java -jar server.jar
```

### para servidor UDP
```Terminal
java -jar udp.jar
```

El servidor escuchara el puerto `5000` para (TCP) 
y `5001` para (UDP) por defecto.

### Conectar un cliente

```Bash
java -jar chat.jar
```

Se te pedira ingresar el nombre de usuario.

---

## Funcionalidades

- [X] Registro de usuario con nombre unico
- [X] Mensaje visibles para todos los conectados
- [X] Mensajes privados entre usuarios (`/Priv <usuario> <mensaje>`)
- [X] Lista de ususarios conectados (`List`)
- [X] Interfaz Grafica

---

## Capturas de pantalla

### Servidor activo
![Sevidor activo](https://github.com/Miguel-1811/Chat-Redes/blob/b2365491f7a1c6f16c1136c6ec6493c43781b603/Resources/servidor_activo.png)

### Registro de usuario
![Registro de usuario](https://github.com/Miguel-1811/Chat-Redes/blob/24ba499fcd08ac61a911ad4809a6ec5ebf5f7031/Resources/registro_usuario.png)

### Chat grupal
![Chat grupal](https://github.com/Miguel-1811/Chat-Redes/blob/60111f5d4eb05099cb9c78de92946499d4172f58/Resources/chat_grupal.png)

### Mensaje privado
![Mensaje privado](https://github.com/Miguel-1811/Chat-Redes/blob/e49268981981c160b7c2152d50d4a9a143302ae8/Resources/mensaje_privado.png)

---

## Protocolo de comunicacion

Los mensajes siguen el siguiente formato:

```
TIPO|ORIGEN|DESTINO|CONTENIDO
```

| Tipo | Descripcion |
|------|-------------|
| `mensaje` | Mesnaje grupal |
| `/Priv <mensaje> <usuario>`   | Mensaje privado |
| `List`    | Lista de ususarios |

---

## Licencia

Proyecto academico - ITSON - Redes - 2026
