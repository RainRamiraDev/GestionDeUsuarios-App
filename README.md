## **API para Gestión de Usuarios - Node.js, TypeScript, GraphQL, Apollo Server y MongoDB**

Presento una solución de API robusta y escalable para la gestión de usuarios, desarrollada con tecnologías modernas y de alto rendimiento. Esta API permite realizar operaciones CRUD completas sobre usuarios con los campos ID, nombre, email y password.

### **Características Clave:**
- **Node.js & TypeScript:** Backend eficiente y fuertemente tipado para mayor rendimiento y mantenimiento.
- **GraphQL & Apollo Server:** Consultas flexibles y poderosas, optimizadas para el rendimiento de tus aplicaciones frontend.
- **MongoDB:** Base de datos NoSQL, ideal para aplicaciones que requieren flexibilidad y escalabilidad.
- **Dockerizado:** Entorno de desarrollo completamente contenedorizado, garantizando una fácil implementación y administración.

Esta solución está diseñada para ser integrada fácilmente en proyectos modernos y ofrece una base sólida para el manejo de usuarios con capacidades de expansión y personalización.



## Configuración para ejecucion desde IDE

1. **Instalar dependencias**

   Ejecuta el siguiente comando para instalar las dependencias del proyecto:

   ```bash
   npm install

2. **Compilar el proyecto**
   ```bash
   npm run build

3. **Ejecutar el proyecto**
   ```bash
   npm run start


## Configuración para ejecucion desde Docker

1. **Descarga la imagen de un contenedor desde un repositorio**
   ```bash
   docker pull rainramira/app-1:latest

2. **Ejecuta la imagen descargada como un contenedor**
   ```bash
   docker run -d -p 4000:4000 --name pepe rainramira/app-1:latest

3. **Lista los contenedores activos**
   ```bash
   docker ps


## Prueba en Apollo-Server
```
[================GET USER (BY ID)====================================]


query {
  getUser(ID: "66e3be140641e70a24eb724f") {
    _id
    name
    email
  }
}


[=================GET USERS (ALL)===================================]


query {
  getUsers(limit: 5) {
    _id
    name
    email
  }
}


[=====================CREATE USER==================================]


 mutation {
  createUser(UserInput: {
    name: "jonathan hola",
    email: "h.hola@gmail.com",
    password: "12345"
  })
}


[===================DELETE USER=================================]


mutation {
  deleteUser(ID: "66e3be140641e70a24eb724f")
}


[==================UPDATE USER===================================]


mutation {
  updateUser(ID: "66e3be140641e70a24eb724f", UserInput: {
    name: "Rain Ramira",
    email: "r.sannarain@gmail.com",
    password: "newpassword123"
  })
}
