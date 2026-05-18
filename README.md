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

---

## Como ejecutar

### Requisitos previos

- Java JDK 17 o superior instalado
- Terminal / Git Bash

### Compilar el proyecto
### Tienes que abrir una terminal dentro de la caroeta donde tengas los jar del proyectoy escribir el siguiente comando
```Bash
java -jar chat.jar
```

### Iniciar el servidor
### para servdiro TCP

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
![Sevidor activo](screenshots/servidor_activo.png)

### Registro de usuario
![Registro de usuario](screenshots/registro_usuario.png)

### Chat grupal
![Chat grupal](screenshots/chat_grupal.png)

### Mensaje privado
![Mensaje privado](screenshots/mensaje_privado.png)

---

## Protocolo de comunicacion

Los mensajes siguen el siguiente formato:

```
TIPO|ORIGEN|DESTINO|CONTENIDO
```

| Tipo | Descripcion |
|------|-------------|
| `mensaje` | Mesnaje grupal |
| `/Priv`   | Mensaje privado |
| `List`    | Lista de ususarios |

---

## Licencia

Proyecto academico - ITSON - Redes - 2026
