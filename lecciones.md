---
layout: page
title: Lecciones aprendidas
permalink: /lecciones/
---

# Algunas lecciones que nos dejo el proyecto


# Problemas encontrados
Durante el transcurso del proyecto nos encontramos con bastantes desafíos, que con tiempo pudimos superar. A continuación mencionamos los más relevantes:

- **Deep Links en Expo**: Uno de los primeros desafíos que enfrentamos fue implementar la funcionalidad de recuperación de contraseñas. Queríamos que el usuario pudiera solicitar un correo para restablecer su contraseña y, desde ese correo, acceder directamente a la pantalla de reseteo en la aplicación. Sin embargo, nos encontramos con una limitación importante: la mayoría de los clientes de correo solo permiten enlaces seguros (https), lo que dificultaba redirigir al usuario directamente a la app.

  Para resolver este problema, diseñamos e implementamos un servidor de redireccionamiento accesible mediante https. Este servidor recibe el path solicitado y redirige al usuario de forma segura hacia la aplicación, permitiendo así una experiencia de recuperación de contraseña fluida y segura.

- **Presentacion de audio**: Durante el proyecto tuvimos entregas parciales donde debiamos presentar los avances en el trabajo. A la hora de compartir audio, tuvimos muchos problemas ya que no todas las aplicaciones implementan AudioPlaybackCapture en android, por lo que no se puede compartir audio en todas las aplicaciones. Pudimos solucionarlo haciendo las reuniones en Discord, aunque no fue la solución ide