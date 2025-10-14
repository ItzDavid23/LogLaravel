## Prerequisites
▪ 🐘 PHP version 8.0 or higher.
▪ ⚙️ Latest stable version of Composer.
▪ 🔺 Laravel installer or create a Laravel project new / composer create-project.
▪ 💻 Local web server package WampServer.
▪ 🌐 Web server: Apache.
▪ 🐬 Running MySQL database.
▪ 📝 Code editor (Visual Studio Code.
▪ 💻 Operating system: Windows 10
▪ Include technology icons.

## Introducción

Este laboratorio tiene como objetivo implementar un sistema de **autenticación de usuarios** utilizando Laravel.  
El proyecto sigue la arquitectura **MVC (Modelo-Vista-Controlador)**:

- **Modelos:** Representan las entidades y se encargan de la lógica relacionada a la base de datos (por ejemplo, `User.php`).  
- **Vistas:** Archivos Blade (`.blade.php`) que representan la interfaz visual para el usuario.  
- **Controladores:** Gestionan la lógica de negocio y coordinan la interacción entre modelos y vistas (por ejemplo, `AuthController`).  
- **Rutas:** Definen la URL y la acción asociada en los controladores (`routes/web.php`).

---

## Flujo de instalación y comandos utilizados

### **Opción 1: Laravel UI**
powershell | bash
- Instalar Laravel/UI
composer require laravel/ui

- Generar scaffolding de autenticación con Bootstrap
php artisan ui bootstrap --auth

- Instalar dependencias de Node y compilar assets
npm install
npm run dev

- Crear las tablas definidas en las migraciones
php artisan migrate

- Limpiar cache de configuración (si es necesario)
php artisan config:cache

- Resultado visual
La imagen muestra la página de login generada automáticamente con Laravel Breeze/UI, incluyendo registro y recuperación de contraseña.

## Base de datos
Servidor: MySQL (WampServer)
Archivo de configuración: .env
.env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=login_laravel
DB_USERNAME=root
DB_PASSWORD=

# Migraciones utilizadas:
- users
- password_resets
- failed_jobs

# Comando para ejecutar migraciones
- php artisan migrate

## Dificultades y soluciones
Problema1:
- Error SQLSTATE[HY000] [1045] Access denied for user 'root'@'localhost'
Solución:
- Verificar usuario y contraseña en .env y reiniciar servidor MySQL.
Problema2:
- Problemas con compilación de assets (npm run dev)
Solución:
- Instalar Node.js y npm correctamente y permitir la ejecución de scripts en
Problema3:
- PowerShell (Set-ExecutionPolicy RemoteSigned).
Solución:
- Carpeta .git embebida dentro del proyecto	Quitar el subrepositorio con git rm --cached <carpeta> para evitar errores al hacer push.

## Referencias
- [Documentación oficial de Laravel](https://laravel.com/docs/10.x)
- [Laravel Breeze](https://laravel.com/docs/10.x/starter-kits#breeze-and-blade)
- [Laravel UI](https://laravel.com/docs/10.x/frontend#laravel-ui)
- [PHP 8](https://www.php.net/releases/8.0/)
- [MySQL](https://chatgpt.com/c/68edaef3-fc98-8328-9a9b-474e49751430)
- [Visual Studio Code](https://chatgpt.com/c/68edaef3-fc98-8328-9a9b-474e49751430)

## Objetivo del laboratorio
El objetivo principal fue implementar autenticación básica en Laravel, comprendiendo la interacción entre controladores, modelos, vistas y rutas, gestionar migraciones, configurar la base de datos y desplegar el proyecto localmente usando WampServer.


## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
>>>>>>> e85d313 (login laravel)
