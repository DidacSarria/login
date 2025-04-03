# 📁 Flujo de trabajo con Git y GitHub Desktop (Markmap)

## 1. 🚀 Inicio del proyecto
- Yo o alguien del grupo crea el proyecto base  
  Ej: login y menú principal
- Copio el archivo `.gitignore` y `README.md` en la raíz de la solución (Visual Studio)
- Abro GitHub Desktop y añado un repositorio local desde la ruta del proyecto  
  - GitHub Desktop detectará que no hay repositorio y me pedirá crear uno nuevo
  - Le asigno un nombre claro y lo inicializo
- Subimos el proyecto a GitHub (rama `main`)

## 2. ⬇️ Clono el proyecto
- Todos descargan el proyecto desde GitHub con GitHub Desktop
- Lo tienen en su ordenador listo para trabajar

## 3. 🌿 Creo mi propia rama
- Desde `main`, creo una nueva rama con mi nombre  
  Ej: `rama-juan`, `rama-marta`
- Así puedo trabajar sin afectar a los demás

## 4. ✍️ Hago mis cambios
- Abro el proyecto en Visual Studio
- Modifico archivos, agrego formularios, programo eventos...

## 5. 💾 Hago commit
- En GitHub Desktop → pestaña “Changes”
- Escribo un mensaje claro  
  Ej: `"Agregado formulario de contacto"`
- Hago click en `Commit to rama-marta`

## 6. ⬆️ Hago push
- Hago click en `Push origin`
- Así mis cambios se suben a mi rama en GitHub

## 7. 🔄 Hago pull antes de trabajar
- Antes de empezar cada día, hago `Pull origin`
- Así me aseguro de tener la última versión del repositorio

## 8. 👀 Quiero ver lo que ha hecho otro compañero
- Si quiero probar el trabajo de otro:
  - Me cambio a su rama (por ejemplo: `rama-lucas`)
  - Hago `merge` de su rama a la mía para probarlo con mi código
- ⚠️ ¡Ojo! Esto no debe confundirse con hacer merge a `main`

## 9. 🔀 Hago merge a `main`
- Cuando mi parte está lista y revisada:
  - Me aseguro de tener los últimos cambios de `main` (`merge` desde `main`)
  - Luego hago `merge` de mi rama a `main`
- Así mi trabajo queda integrado oficialmente

## 10. 🪄 Cambio de rama con cambios sin guardar
- Si tengo cambios pendientes sin guardar (sin commit)
- GitHub Desktop me pregunta si quiero moverlos
- Puedo crear una nueva rama y seguir ahí

## 11. 📥 Guardo cambios con stash (automático)
- GitHub Desktop no usa el comando `stash` como tal
- Pero si intento cambiar de rama con cambios pendientes, me da dos opciones:
  - Mover los cambios a la nueva rama
  - O quedarme y hacer commit primero

## 🔁 Ejemplo 1: Trabajo individual en mi rama
- Yo edito `frmLogin.cs` en `rama-marta`
- Antes de empezar, hago `merge` desde `main` a mi rama para tener lo último
- Hago `commit` con mensaje: `"Validación de contraseña"`
- Hago `push`
- Cuando termino y he probado que todo funciona, hago `merge` de `rama-marta` a `main`
- Cambio de nuevo a `rama-marta` y hago `merge` desde `main` para ponerme al día si otros han subido algo nuevo
- Si no hay nada nuevo, GitHub Desktop me dirá que mi rama ya está actualizada

## 🔁 Ejemplo 2: Trabajo conjunto con código de otro
- Estoy en `rama-carmen`, y necesito lo que ha hecho Lucas en `rama-lucas`
- Hago `merge` desde `rama-lucas` a `rama-carmen` para combinar su parte con la mía
- Como `rama-lucas` aún no está integrada en `main`, yo sí tendré los cambios de Lucas pero él no los tendrá hasta que hagamos merge a `main`
- Si además necesito ponerme al día con `main`, puedo hacer `merge` desde `main` a `rama-carmen` antes o después para no perderme ningún cambio adicional
- Pruebo todo junto en `rama-carmen`
- Si todo va bien, hago `commit`, `push` y luego `merge` de `rama-carmen` a `main`
- Finalmente, vuelvo a mi rama (`rama-carmen`) y hago `merge` desde `main` para sincronizarla con lo oficial

## ✅ Reglas clave
- Hago `pull` antes de empezar
- Siempre trabajo en mi propia rama
- Uso mensajes claros en cada `commit`
- Hago `push` al terminar mi parte
- Verifico que todo funciona antes del `merge` final

---

## ⚙️ Configuración personalizada en `.gitignore`

### 🟡 Carpeta Help de documentación Sandcastle
- Ignorar todo lo de `NombreDeTuProyectoSandcastle/Help`
```
NombreDeTuProyectoSandcastle/Help/**
NombreDeTuProyectoSandcastle/Help/*
```

### 🔵 Carpeta de compilación (App)
- Ignorar todos los archivos en la raíz:
```
App/*
```
- Permitir carpetas dentro de `App`:
```
!App/**/
```
- Permitir archivos dentro de subcarpetas:
```
!App/*/**
```
