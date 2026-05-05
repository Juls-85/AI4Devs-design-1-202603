# Documentación de Producto: LTI - El ATS del Futuro

## 1. Descripción del Software, Valor Añadido y Ventajas Competitivas

**LTI (Lead Talent Intelligence)** es una plataforma SaaS de próxima generación diseñada para transformar el ciclo de vida del reclutamiento. A diferencia de los ATS tradicionales que actúan como simples bases de datos, LTI es un motor de inteligencia activa.

### Valor Añadido
LTI elimina la carga administrativa de los departamentos de RRHH mediante el uso de **IA Generativa y Predictiva**, permitiendo que los reclutadores se centren en lo que importa: la conexión humana.

### Ventajas Competitivas
1.  **IA Nativa (No un parche):** Clasificación automática de candidatos basada en fit cultural y técnico real, no solo palabras clave.
2.  **Colaboración en Tiempo Real:** Interfaz tipo "War Room" donde managers y reclutadores interactúan sobre perfiles en vivo.
3.  **Automatización Hiper-Personalizada:** Workflows que envían mensajes personalizados y programan entrevistas sin intervención humana.
4.  **Analítica Predictiva:** Predice el tiempo de contratación y la probabilidad de retención del candidato.

---

## 2. Funciones Principales

-   **AI Sourcing & Screening:** Análisis automático de CVs y perfiles sociales con ranking de relevancia.
-   **Collaborative Hiring Hub:** Chat integrado, sistema de votación rápida y feedback compartido en fichas de candidato.
-   **Smart Scheduling:** Integración con calendarios para autoprogramación de entrevistas basadas en disponibilidad de ambas partes.
-   **Automated Pipeline Triggers:** Movimiento automático de candidatos entre fases basado en evaluaciones o tests técnicos.
-   **IA Co-Pilot:** Redacción de descripciones de puesto y correos electrónicos con tono de marca ajustable.

---

## 3. Lean Canvas

| **Problema** | **Solución** | **Propuesta Única de Valor** | **Ventaja Especial** | **Segmentos de Cliente** |
| :--- | :--- | :--- | :--- | :--- |
| - Procesos lentos y manuales.<br>- Falta de comunicación Reclutador-Manager.<br>- Sesgos en la selección. | - Automatización con IA.<br>- Panel colaborativo en tiempo real.<br>- Screening ciego opcional. | El único ATS que piensa por ti: Automatización total desde el sourcing hasta la oferta. | Algoritmo de matching propietario basado en Machine Learning profundo. | Startups tecnológicas y empresas medianas en crecimiento. |
| **Alternativas Existentes** | **Métricas Clave** | **Canales** | **Estructura de Costes** | **Flujos de Ingresos** |
| ATS tradicionales (Greenhouse, Lever), Excel. | Time-to-hire, Cost-per-hire, Candidate Experience Score. | Ventas directas (B2B), LinkedIn Ads, Content Marketing. | Desarrollo software (Cloud), Salarios, Marketing/Ventas. | Suscripción mensual por usuario (SaaS), Tier por volumen de vacantes activas. |

**Diagrama:**
```mermaid
graph TD
    subgraph LeanCanvas [Lean Canvas: ATS con IA]
        direction TB

        P["<b>1. Problema</b><br/>- Procesos lentos y manuales<br/>- Falta comunicación Rec-Mgr<br/>- Sesgos en selección<br/><hr/><i>Alt: ATS (Greenhouse), Excel</i>"] 
        
        S["<b>2. Solución</b><br/>- Automatización con IA<br/>- Panel colaborativo RT<br/>- Screening ciego opcional"]

        PUV["<b>3. Propuesta Única de Valor</b><br/>El único ATS que piensa por ti:<br/>Automatización total de sourcing a oferta"]

        VE["<b>4. Ventaja Especial</b><br/>Algoritmo de matching propietario<br/>basado en Machine Learning profundo"]

        SC["<b>5. Segmentos de Cliente</b><br/>Startups tecnológicas y<br/>empresas medianas en crecimiento"]

        MC["<b>6. Métricas Clave</b><br/>- Time-to-hire<br/>- Cost-per-hire<br/>- Candidate Experience Score"]

        C["<b>7. Canales</b><br/>- Ventas directas (B2B)<br/>- LinkedIn Ads<br/>- Content Marketing"]

        EC["<b>8. Estructura de Costes</b><br/>Desarrollo Cloud, Salarios,<br/>Marketing y Ventas"]

        FI["<b>9. Flujos de Ingresos</b><br/>Suscripción SaaS mensual,<br/>Tier por volumen de vacantes"]

    end

    %% Conexiones
    P --- S
    S --- PUV
    PUV --- VE
    VE --- SC
    MC --- PUV
    C --- SC
    EC --- FI
    
    style PUV fill:#f96,stroke:#333,stroke-width:2px
    style VE fill:#dfd,stroke:#333
    style SC fill:#dff,stroke:#333
```
---

## 4. Casos de Uso Principales

### Caso de Uso 1: Cribado Automático con IA
**Actor:** Reclutador / Sistema IA.
**Descripción:** El sistema analiza 500 aplicaciones recibidas, extrae entidades clave y puntúa a los candidatos del 1 al 100 según el Job Description.

**Diagrama:**
```mermaid
graph LR
    %% Definición de Actores
    subgraph Actores
        R((Reclutador))
        IA((Sistema IA))
    end

    %% Límites del Sistema
    subgraph "Sistema ATS (Módulo de Cribado)"
        UC1([<b>CU1: Cribado Automático con IA</b>])
        
        %% Pasos internos detallados
        Step1[Analizar 500 aplicaciones]
        Step2[Extraer entidades clave]
        Step3[Puntuar candidatos 1-100]
        
        UC1 --- Step1
        UC1 --- Step2
        UC1 --- Step3
    end

    %% Relaciones
    R --- UC1
    IA --- UC1

    %% Estilos para que parezca un diagrama de caso de uso
    style UC1 fill:#f9f,stroke:#333,stroke-width:2px
    style R fill:#fff,stroke:#333
    style IA fill:#fff,stroke:#333
```

### Caso de Uso 2: Colaboración en Tiempo Real para Feedback
**Actor:** Hiring Manager y Reclutador.
**Descripción:** Durante una revisión, el Manager deja un comentario y una puntuación en la ficha del candidato; el Reclutador recibe notificación instantánea y decide mover al candidato a "Oferta" inmediatamente.

**Diagrama:**
```mermaid
graph LR
    %% Definición de Actores con iconos de círculo
    HM((Hiring Manager))
    REC((Reclutador))

    subgraph "Módulo de Colaboración"
        %% Caso de Uso Principal (Forma de elipse)
        UC2([<b>CU2: Colaboración en Tiempo Real</b>])
        
        %% Acciones detalladas
        A1[Dejar Comentario y Puntuación]
        A2[Recibir Notificación Instantánea]
        A3[Mover a Candidato a Oferta]
        
        %% Flujo interno
        UC2 --- A1
        A1 -.-> A2
        A2 -.-> A3
    end

    %% Relaciones de los Actores con el Caso de Uso
    HM --- UC2
    REC --- UC2

    %% Estilos para mayor claridad
    style UC2 fill:#e1f5fe,stroke:#01579b,stroke-width:2px
    style HM fill:#fff,stroke:#333
    style REC fill:#fff,stroke:#333
    style A3 fill:#c8e6c9,stroke:#2e7d32
```

### Caso de Uso 3: Programación de Entrevistas Automatizada
**Actor:** Candidato y Sistema.
**Descripción:** Tras ser aprobado, el sistema envía un link al candidato con los huecos libres del equipo; el candidato elige uno y se crea la reunión en Google Meet/Zoom automáticamente.

**Diagrama:**
```mermaid
graph LR
    subgraph "Sistema de Programación"
        UC1(Enviar link de disponibilidad)
        UC2(Seleccionar hueco libre)
        UC3(Crear reunión Meet/Zoom)
    end

    Candidato((Candidato))
    Sistema((Sistema))

    Sistema --> UC1
    UC1 --> Candidato
    Candidato --> UC2
    UC2 --> UC3
    UC3 --> Sistema
```

---

## 5. Modelo de Datos

| Entidad | Atributo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| **User** (Recruiter/Manager) | id | UUID (PK) | Identificador único. |
| | name | String | Nombre completo. |
| | role | Enum | ADMIN, RECRUITER, MANAGER. |
| **Job_Opening** | id | UUID (PK) | Identificador de la vacante. |
| | title | String | Título del puesto. |
| | status | Enum | OPEN, CLOSED, DRAFT. |
| **Candidate** | id | UUID (PK) | Identificador del candidato. |
| | full_name | String | Nombre del candidato. |
| | email | String | Correo electrónico. |
| | ai_score | Float | Puntuación asignada por la IA. |
| **Application** | id | UUID (PK) | Relación candidato-vacante. |
| | job_id | UUID (FK) | Referencia a Job_Opening. |
| | candidate_id | UUID (FK) | Referencia a Candidate. |
| | stage | String | Fase actual (Sourcing, Interview, etc). |
| **Comment** | id | UUID (PK) | Comentarios de colaboración. |
| | application_id | UUID (FK) | Referencia a la aplicación. |
| | author_id | UUID (FK) | Referencia al usuario. |
| | content | Text | Contenido del feedback. |

**Relaciones:**
- Un **User** puede crear muchas **Job_Openings** (1:N).
- Una **Job_Opening** tiene muchas **Applications** (1:N).
- Un **Candidate** puede tener varias **Applications** (1:N).
- Una **Application** tiene muchos **Comments** (1:N).

**Diagrama**
```mermaid
erDiagram
    USER ||--o{ JOB_OPENING : "crea"
    USER ||--o{ COMMENT : "escribe"
    JOB_OPENING ||--o{ APPLICATION : "contiene"
    CANDIDATE ||--o{ APPLICATION : "realiza"
    APPLICATION ||--o{ COMMENT : "recibe"

    USER {
        UUID id PK
        String name
        Enum role
    }

    JOB_OPENING {
        UUID id PK
        String title
        Enum status
        UUID creator_id FK
    }

    CANDIDATE {
        UUID id PK
        String full_name
        String email
        Float ai_score
    }

    APPLICATION {
        UUID id PK
        UUID job_id FK
        UUID candidate_id FK
        String stage
    }

    COMMENT {
        UUID id PK
        UUID application_id FK
        UUID author_id FK
        Text content
    }
```

---

## 6. Diseño del Sistema a Alto nivel

LTI utiliza una arquitectura de **Microservicios** desplegada en la nube (AWS/Azure) para garantizar escalabilidad.

-   **Frontend:** Single Page Application (React/Next.js) para una experiencia fluida.
-   **API Gateway:** Gestiona la autenticación y el enrutamiento.
-   **Servicio de Candidatos:** Gestiona perfiles y documentos.
-   **Motor de IA (Worker):** Procesa CVs de forma asíncrona usando colas de mensajes (RabbitMQ/Kafka).
-   **Notificaciones en Tiempo Real:** Websockets para el Hub colaborativo.

**Diagrama**
```mermaid
graph TD
    %% Definición de Actores y Frontend
    User((Usuario/Reclutador)) -->|Interactúa| FE[Frontend: React/Next.js]
    
    %% Gateway y Seguridad
    FE -->|Solicitudes HTTPS| GW[API Gateway]
    GW -.->|Auth & Routing| GW
    
    %% Microservicios
    subgraph "Nube (AWS/Azure)"
        GW -->|API Calls| CS[Servicio de Candidatos]
        GW -->|Pub/Sub| WS[Servicio de Notificaciones]
        
        %% Componentes de Datos y Mensajería
        CS -->|Almacena CVs| DB[(Base de Datos)]
        CS -->|Publica evento| MQ{Message Queue: RabbitMQ/Kafka}
        
        %% Procesamiento Asíncrono
        MQ -->|Consume mensajes| AI[Motor de IA: Worker]
        AI -->|Actualiza resultados| DB
        AI -->|Notifica fin de proceso| MQ
        
        %% Real-Time
        WS <-->|Websockets| FE
    end

    %% Estilos
    style FE fill:#f9f,stroke:#333,stroke-width:2px
    style GW fill:#bbf,stroke:#333,stroke-width:2px
    style AI fill:#dfd,stroke:#333,stroke-width:2px
    style MQ fill:#ffe,stroke:#333,stroke-width:2px
    style DB fill:#eee,stroke:#333,stroke-width:2px
```

---

## 7. Diagrama C4 (Nivel 3: Componentes del API Service)

Nos enfocamos en el **"AI Matching Service"**, el corazón de LTI.

1.  **Job Parser:** Extrae requisitos técnicos y soft skills de la descripción del puesto.
2.  **Resume Extractor:** Procesa archivos PDF/Docx usando OCR e IA.
3.  **Vector Database (Pinecone/Milvus):** Almacena representaciones numéricas de perfiles para búsqueda semántica.
4.  **Matching Engine:** Algoritmo que calcula la distancia entre el vector del candidato y el del puesto.
5.  **Audit Logger:** Registra las decisiones de la IA para evitar sesgos y permitir explicabilidad.

**Diagrama**
```mermaind
graph TB
    %% Definición de elementos externos al servicio
    API_GW[API Gateway]
    MQ[Message Queue: RabbitMQ/Kafka]
    DB_SQL[(Relational DB)]

    subgraph AI_Matching_Service [Component: AI Matching Service]
        direction TB
        
        JP[Job Parser]
        RE[Resume Extractor]
        ME[Matching Engine]
        VD[(Vector Database: Pinecone/Milvus)]
        AL[Audit Logger]

        %% Flujo de datos interno
        JP -->|Requisitos extraídos| ME
        RE -->|Perfil extraído| ME
        RE -->|Embeddings| VD
        ME <-->|Búsqueda semántica| VD
        ME -->|Cálculo de Score| AL
    end

    %% Relaciones externas
    API_GW --> JP
    MQ --> RE
    AL --> DB_SQL
    ME -->|Resultados finales| API_GW

    %% Estilos
    style AI_Matching_Service fill:#f5f5f5,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5
    style VD fill:#e1f5fe,stroke:#01579b
    style AL fill:#fff3e0,stroke:#e65100
```
---
Fin de la propuesta
