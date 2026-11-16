# DriveEasy · Configuration centralisée

Fichiers de configuration lus par le **Config Server** du projet
[driveeasy-backend](https://github.com/mohamedbenhassin-design/driveeasy-backend) lorsqu'il est lancé avec le profil `git` :

```bash
java -jar config-server/target/config-server-1.0.0.jar --spring.profiles.active=git
```

| Fichier | Contenu |
|---|---|
| `application.yml` | Commun : Eureka, Actuator, Zipkin (échantillonnage 1.0), format des logs |
| `application-prod.yml` | Profil `prod` : échantillonnage 10 %, pas de données de démonstration |
| `vehicule-service.yml` | Port 8081, stockage en mémoire |
| `client-service.yml` | Port 8082, âge minimum |
| `location-service.yml` | Port 8083, tarification (coefficients, remises, pénalité, seuils de fidélité) |
| `api-gateway.yml` | Port 8080, routes `lb://`, CORS |
