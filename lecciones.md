---
layout: page
title: Lecciones aprendidas
permalink: /lecciones/
---

# Algunas lecciones que nos dejo el proyecto
A lo largo del desarrollo de Espotifai, nos enfrentamos a diversos desafíos técnicos y organizativos que nos permitieron crecer como equipo y mejorar nuestras habilidades. En esta sección compartimos los principales problemas encontrados y las lecciones que aprendimos, con el objetivo de que sirvan de referencia para futuros proyectos.
- **Importancia de la planificación**: Finalizado el trabajo podemos decir que la división en entregas parciales (Checkpoints) fue una buena forma de organizar el proyecto. Nos permitió estimar mejor el trabajo necesario por semana e ir creciendo la aplicación incrementalmente.
- **Detectar las dependencias**: En uno de estos checkpoints, algunas funcionalidades dependian de otras para poder implementarse, lo que nos atraso un poco el desarrollo. Nos queda como lección el analizar con más detalle las funcionalidades a implementar para detectar si hay dependencias.
- **El esfuerzo inicial**: Notamos que la etapa más demandante del proyecto fue al principio, cuando tuvimos que definir la estructura general, configurar los entornos de desarrollo, integrar las tecnologías y establecer las bases para los microservicios. Esta fase requirió mucha coordinación y toma de decisiones, pero facilitó el trabajo en las etapas posteriores al contar con una base sólida y bien organizada.

# Problemas encontrados
Durante el transcurso del proyecto nos encontramos con bastantes desafíos, que con tiempo pudimos superar. A continuación mencionamos los más relevantes:

- **Deep Links en Expo**: Uno de los primeros desafíos que enfrentamos fue implementar la funcionalidad de recuperación de contraseñas. Queríamos que el usuario pudiera solicitar un correo para restablecer su contraseña y, desde ese correo, acceder directamente a la pantalla de reseteo en la aplicación. Sin embargo, nos encontramos con una limitación importante: la mayoría de los clientes de correo solo permiten enlaces seguros (https), lo que dificultaba redirigir al usuario directamente a la app.

  Para resolver este problema, diseñamos e implementamos un servidor de redireccionamiento accesible mediante https. Este servidor recibe el path solicitado y redirige al usuario de forma segura hacia la aplicación, permitiendo así una experiencia de recuperación de contraseña fluida y segura.

- **Presentacion de audio**: Durante el proyecto tuvimos entregas parciales donde debiamos presentar los avances en el trabajo. A la hora de compartir audio, tuvimos muchos problemas ya que no todas las aplicaciones implementan AudioPlaybackCapture en android, por lo que no se puede compartir audio en todas las aplicaciones. Pudimos solucionarlo haciendo las reuniones en Discord, aunque no fue la solución ide