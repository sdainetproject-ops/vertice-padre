# Vértice Padre (`vertice-padre`)

Proyecto padre de Maven (**POM padre**) diseñado para centralizar la configuración del ciclo de vida de construcción, gestión de versiones, dependencias y plugins en los módulos del ecosistema **Vértice**.

---

## 🚀 Tecnologías y Requisitos

* **Java:** 21 (LTS)
* **Framework:** [Quarkus](https://quarkus.io/) `3.39.3` (`quarkus-bom`)
* **Gestor de Construcción:** Apache Maven 3.9+
* **Empaquetado:** `pom` (Multi-módulo)

---

## 📦 Estructura y Módulos

Este repositorio actúa como agregador y definidor de dependencias para los siguientes módulos:

* `vertice-prueba`
* *(Futuros módulos del ecosistema Vértice)*

---

## 🛠️ Configuración y Dependencias Centralizadas

El proyecto proporciona configuraciones predeterminadas para:

### 1. Inyección de Dependencias y REST
* `quarkus-arc`: Contexts and Dependency Injection (CDI).
* `quarkus-rest`: Soporte para desarrollo de APIs REST reactivas.

### 2. Testing y Calidad
* `quarkus-junit`: Soporte para pruebas unitarias y de integración en Quarkus.
* `rest-assured`: Framework para testing de servicios HTTP/REST.
* `maven-surefire-plugin` y `maven-failsafe-plugin` para pruebas unitarias e integración.

### 3. Compilación y Construcción Nativa
* `maven-compiler-plugin`: Configurado para Java 21 (`<maven.compiler.release>21</maven.compiler.release>`).
* **Perfil Nativo (`-Pnative`):** Soporte para compilar a binario nativo con GraalVM / Mandrel.

---

## 💻 Comandos Útiles

### Compilar y verificar el proyecto
```bash
mvn clean compile
```

### Ejecutar pruebas
```bash
mvn test
```

### Compilar perfil nativo
```bash
mvn clean package -Pnative
```

---

## 🏷️ Versionado

* **Versión actual:** `1.0.0.0-RELEASE`
* **Grupo:** `sdai.com.sis`
* **Artefacto:** `vertice-padre`