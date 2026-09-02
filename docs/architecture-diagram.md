# System Architecture Diagram

## High-Level Workflow

```mermaid
graph TD
    A[Discovery Contract] --> B[Execution Engine<br/>Provider-Neutral]
    B --> C[Verification Gates]
    C --> D[Release Attestation]
    
    subgraph "Input Layer"
        A1[API Contract<br/>synthetic-contract.json]
        A2[Request Schema]
        A3[Evidence Requirements]
        A4[Security Constraints]
    end
    
    subgraph "Processing Layer"
        B1[Route Resolution<br/>No Vendor SDK]
        B2[Policy Application<br/>Refusal Rules]
        B3[Artifact Generation]
    end
    
    subgraph "Verification Layer"
        C1[Schema Validation]
        C2[Secret Detection]
        C3[Hash Recording]
        C4[Compliance Check]
    end
    
    subgraph "Output Layer"
        D1[Structured Response]
        D2[Evidence Package]
        D3[Audit Trail]
        D4[Release Artifact]
    end
    
    A1 --> B1
    A2 --> B1
    A3 --> C1
    A4 --> C2
    B1 --> B2
    B2 --> B3
    B3 --> C1
    B3 --> C2
    C1 --> C3
    C2 --> C3
    C3 --> C4
    C4 --> D1
    C4 --> D2
    C4 --> D3
    C4 --> D4
```

## Security Boundary Model

```mermaid
graph TB
    subgraph "Public Proof Repository"
        P1[Synthetic Contracts]
        P2[Example Inputs/Outputs]
        P3[Security Model Doc]
        P4[Evidence Structure]
    end
    
    subgraph "Security Boundary 🔒"
        B1[No API Keys]
        B2[No Customer Data]
        B3[No Provider SDKs]
        B4[No Production URLs]
        B5[No Private Prompts]
    end
    
    subgraph "Private Core (Not Published)"
        R1[Runtime Engine]
        R2[Orchestration Logic]
        R3[Provider Adapters]
        R4[Customer Integrations]
        R5[Deployment Config]
    end
    
    P1 -.->|Reference Only| R1
    P2 -.->|Shape Example| R1
    P3 -.->|Policy Guide| R2
    P4 -.->|Structure Spec| R2
    
    B1 --> R1
    B2 --> R1
    B3 --> R2
    B4 --> R3
    B5 --> R2
```

## Evidence Flow

```mermaid
sequenceDiagram
    participant U as User/Team
    participant D as Discovery Kit
    participant E as Execution Engine
    participant V as Verification Gates
    participant A as Attestation Store
    
    U->>D: Submit workflow contract
    D->>E: Forward with metadata
    E->>E: Apply provider-neutral routing
    E->>V: Send artifact + evidence requirements
    V->>V: Run schema validation
    V->>V: Run secret detection
    V->>V: Record artifact hash
    V->>A: Store verification result
    A->>U: Return attestation package
    
    Note over U,A: All steps produce<br/>machine-readable evidence
```

## Pilot Engagement Flow

```mermaid
graph LR
    A[Initial Contact] --> B[Discovery Call]
    B --> C{Qualified?}
    C -->|Yes| D[Define Baseline]
    C -->|No| E[Archive Lead]
    D --> F[Select Workflow]
    F --> G[2-Week Pilot]
    G --> H[Measure Results]
    H --> I{Success?}
    I -->|Yes| J[Expand Scope]
    I -->|No| K[Document Learnings]
    J --> L[Production Agreement]
    K --> E
```

## Component Responsibilities

| Component | Responsibility | Public Evidence | Private Implementation |
|-----------|---------------|-----------------|----------------------|
| **Discovery Contract** | Define workflow scope, inputs, outputs, constraints | ✅ `synthetic-contract.json` | ❌ Customer-specific templates |
| **Execution Engine** | Route requests without vendor lock-in | ✅ Provider-neutral design doc | ❌ Runtime orchestration code |
| **Verification Gates** | Validate schema, detect secrets, record hashes | ✅ Evidence structure spec | ❌ Validation implementation |
| **Attestation Store** | Store and retrieve verification results | ✅ Sample output format | ❌ Storage backend, APIs |
| **Security Model** | Define refusal rules and boundaries | ✅ `security-model.md` | ❌ Enforcement mechanisms |

## Data Classification Model

```
┌─────────────────────────────────────────────────────────────┐
│                    DATA CLASSIFICATION                       │
├──────────────┬──────────────┬──────────────┬────────────────┤
│   PUBLIC     │   SYNTHETIC  │   INTERNAL   │   CONFIDENTIAL │
├──────────────┼──────────────┼──────────────┼────────────────┤
│ README.md    │ Contracts    │ Runtime      │ Customer Data  │
│ Security Doc │ Demo IDs     │ Prompts      │ API Keys       │
│ Examples     │ Fake Payloads│ Config       │ Production URLs│
│ License      │ Test Outputs │ Integrations │ Credentials    │
└──────────────┴──────────────┴──────────────┴────────────────┘
         │              │              │              │
         ▼              ▼              ▼              ▼
    GitHub Public   This Repo     Private Repo    Never Stored
```

---

*This diagram is for understanding the system architecture. Actual implementation details are in the private core repository.*
