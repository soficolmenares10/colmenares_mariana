# 🚀 Instalación de Git Flow en Windows

## 📖 Descripción

En este documento se explica el proceso de instalación de Git Flow en Windows utilizando Scoop como gestor de paquetes, debido a que el método tradicional con curl presentó errores de certificados SSL.

---

## 🛠️ Herramientas utilizadas

- Git
- Git Bash
- PowerShell
- Scoop (gestor de paquetes para Windows)
- git-flow-next

---

## ⚙️ Paso 1: Verificar instalación de Git

Se verificó que Git estuviera instalado ejecutando:

```bash
git --version
⚙️ Paso 2: Instalación de Scoop

Se abrió PowerShell como administrador y se ejecutaron los siguientes comandos:

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
iwr -useb get.scoop.sh | iex

Esto instaló Scoop correctamente.

⚙️ Paso 3: Agregar buckets necesarios

Se agregaron los repositorios (buckets) necesarios:

scoop bucket add main
scoop bucket add extras
⚙️ Paso 4: Búsqueda del paquete correcto

Al intentar instalar git-flow, apareció el error:

Couldn't find manifest for 'git-flow'

Se realizó una búsqueda con:

scoop search git-flow

El resultado mostró que el paquete disponible era:

git-flow-next
⚙️ Paso 5: Instalación de Git Flow

Se instaló correctamente con:

scoop install git-flow-next
✅ Paso 6: Verificación de instalación

Desde Git Bash se verificó con:

git flow version

Si muestra la versión, la instalación fue exitosa.

🎯 Resultado

Git Flow quedó instalado correctamente en Windows utilizando Scoop y el paquete actualizado git-flow-next.