# CI/CD Demo - Spring Boot

![CI](https://github.com/TU_USUARIO/cicd-demo-springboot/actions/workflows/ci.yml/badge.svg)

## Descripción

Proyecto de demostración de CI/CD con Spring Boot, GitHub Actions, JaCoCo y Maven.

## Características

- ✅ Pipeline de CI/CD automatizado con GitHub Actions
- ✅ Pruebas unitarias con JUnit 5
- ✅ Reporte de cobertura de código con JaCoCo
- ✅ Separación de jobs (build y test)
- ✅ Protección de ramas

## Endpoints

- `GET /api/sum?a=3&b=4` - Suma dos números
- `GET /api/multiply?a=3&b=4` - Multiplica dos números
- `GET /api/health-check` - Verifica el estado de la aplicación

## Requisitos

- Java 21
- Maven 3.8+

## Ejecución Local

```bash
# Compilar
mvn clean package

# Ejecutar pruebas
mvn test

# Ejecutar con cobertura
mvn verify

# Ejecutar la aplicación
mvn spring-boot:run
```

## Pipeline CI/CD

El pipeline se ejecuta automáticamente en:

- Push a `main` o `develop`
- Pull requests a `main`

### Pasos del Pipeline

1. **Build**: Compila y empaqueta la aplicación
2. **Test**: Ejecuta las pruebas unitarias
3. **Coverage**: Genera reporte de cobertura con JaCoCo
4. **Artifacts**: Guarda reportes por 7 días

## Protección de Ramas

La rama `main` está protegida y requiere que el pipeline pase antes de hacer merge.

---

**Nota**: Reemplaza `TU_USUARIO` en el badge con tu usuario de GitHub.
