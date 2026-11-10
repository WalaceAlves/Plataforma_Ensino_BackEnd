# Plataforma de Ensino - Backend

Este repositório contém a API REST para a plataforma de aprendizagem online.

## Modelo de Dados (Diagrama ER)

Abaixo está a representação visual das entidades e seus relacionamentos no banco de dados:

```mermaid
erDiagram
    USER ||--o{ ENROLLMENT : "matricula-se em"
    USER ||--o{ CERTIFICATION : "conquista"
    USER ||--o{ COURSE : "leciona (instrutor)"
    CATEGORY ||--o{ COURSE : "agrupa"
    COURSE ||--o{ LESSON : "contem"
    COURSE ||--|{ ENROLLMENT : "possui matriculas"
    COURSE ||--o| ASSESSMENT : "possui prova"
    COURSE ||--o{ CERTIFICATION : "emite"
    ASSESSMENT ||--o{ QUESTION : "possui"
