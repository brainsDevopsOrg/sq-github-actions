# Integración de Github Actions y SonarQube

Este repositorio contiene un ejemplo de cómo integrar [Sonarqube](https://docs.sonarsource.com/sonarqube/10.3/) con [Github Actions](https://docs.github.com/es/actions) ejecutando Sonarqube en local y exponiéndolo al exterior con [ngrok](https://ngrok.com/)

## Contexto
Este repositorio forma parte del contenido de mi curso de udemy:
* [Domina Sonarqube](https://www.udemy.com/course/domina-sonarqube/?referralCode=EF59257E7D8DC3026D6D)

Si te interesa aprender más sobre Sonarqube o Github Actions, Puedes ver si hay promociones vigentes para los cursos en la sección de cursos de [devopsbrains.com](https://devopsbrains.com/cursos/)

# Uso del ejemplo
* Crea un fork de este repositorio en tu cuenta de Github
* Puedes lanzar SonarQube y ngrok en local siguiendo las instrucciones de este otro [repositorio](https://github.com/BrainsDevOps/sonarqube-udemy-docker-compose)
* Crea un token para el análisis de proyectos en tu instancia local de [SonarQube](http://localhost:9000/account/security)
* Crea secretos para tu url y token de sonar para tu repositorio de Github
    * SONAR_TOKEN - El token que acabas de generar en el apartado de seguridad de SonarQube
    * SONAR_HOST_URL - Tu dominio de ngrok, donde estás exponiendo Sonarqube en Internet
* Lanza la acción en el apartado "Actions" de tu repositorio en Github. Con un push a la rama main o manualmente
* Si todo sale bien, deberías de poder consultar el resultado en tu instancia de [SonarQube](http://localhost:9000/dashboard?id=github-actions)