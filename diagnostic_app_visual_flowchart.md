# Diagnostic App - Visual Flowcharts (Mermaid)

## Mobile App User Flow

### 1. Complete Mobile App Navigation Flow
```mermaid
graph TD
    A[Splash Screen] --> B[Login/Signup Screen]
    B --> B1[Login]
    B --> B2[Signup]
    B --> B3[Forgot Password]
    B --> B4[Reset via Email]
    
    B1 --> C[Home Screen]
    B2 --> C
    B4 --> C
    
    C --> D[Start Diagnosis]
    C --> E[Past Reports]
    C --> F[Recommendations]
    C --> G[Profile & Settings]
    
    %% Start Diagnosis Flow
    D --> D1[Symptom Selection]
    D1 --> D2[Step 1: Enter Symptoms & Details]
    D2 --> D3[Step 2: Additional Questions]
    D3 --> D4[Step 3: Attachments/Reports]
    D4 --> D5[Review & Submit]
    D5 --> D6[View Diagnosis Result]
    D6 --> D7[View/Edit Profile]
    D6 --> D8[Block User/Report Issue]
    
    %% Past Reports Flow
    E --> E1[List of Previous Diagnoses]
    E1 --> E2[View Full Report]
    E2 --> E3[Edit/Update Report]
    E2 --> E4[Export as PDF/CSV]
    E2 --> E5[Delete Report]
    
    %% Recommendations Flow
    F --> F1[View Recommended Actions]
    F --> F2[Medication Guidance]
    F --> F3[Dosage & Duration Instructions]
    F --> F4[Disease & Symptom Education]
    
    %% Profile & Settings Flow
    G --> G1[Edit Profile Information]
    G --> G2[Change Password]
    G --> G3[Notification Preferences]
    G --> G4[Language Selection]
    G --> G5[Dark Mode]
    G --> G6[Export Data]
    
    %% Styling
    classDef primaryFlow fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    classDef secondaryFlow fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px
    classDef actionFlow fill:#e8f5e8,stroke:#388e3c,stroke-width:2px
    
    class A,B,C primaryFlow
    class D,D1,D2,D3,D4,D5,D6 secondaryFlow
    class E,E1,E2,F,F1,F2,G,G1,G2 actionFlow
```

### 2. Detailed Diagnosis Process Flow
```mermaid
graph TD
    A[Start Diagnosis] --> B[Symptom Selection Interface]
    B --> C{User Selects Symptoms}
    C --> D[Step 1: Enter Symptoms & Details]
    
    D --> E[Symptom Details Form]
    E --> F[Duration Input]
    F --> G[Severity Rating]
    G --> H[Location/Body Part]
    
    H --> I{Additional Questions Needed?}
    I -->|Yes| J[Step 2: Additional Questions]
    I -->|No| M[Step 3: Attachments]
    
    J --> K[Follow-up Questions]
    K --> L[Symptom Correlations]
    L --> M[Step 3: Attachments]
    
    M --> N{Upload Files?}
    N -->|Yes| O[Upload Images/Reports]
    N -->|No| P[Review & Submit]
    O --> P
    
    P --> Q[Data Validation]
    Q --> R{Valid Data?}
    R -->|No| S[Show Errors]
    S --> D
    R -->|Yes| T[Process Diagnosis]
    
    T --> U[Diagnostic Algorithm]
    U --> V[Generate Results]
    V --> W[View Diagnosis Result]
    
    W --> X[Treatment Recommendations]
    W --> Y[Educational Content]
    W --> Z[Save to History]
    
    %% Styling
    classDef startEnd fill:#ffcdd2,stroke:#d32f2f,stroke-width:3px
    classDef process fill:#c8e6c9,stroke:#388e3c,stroke-width:2px
    classDef decision fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    classDef data fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    
    class A,W startEnd
    class B,D,E,F,G,H,J,K,L,M,O,P,Q,T,U,V,X,Y,Z process
    class C,I,N,R decision
```

## Admin Panel Flow

### 1. Complete Admin Panel Navigation Flow
```mermaid
graph TD
    A[Admin Login] --> B{Authentication}
    B -->|Success| C[Dashboard]
    B -->|Failed| D[Login Error]
    B -->|2FA Required| E[Two-Factor Authentication]
    
    D --> A
    E --> C
    
    C --> F[User Management]
    C --> G[Content Management]
    C --> H[System Configuration]
    C --> I[Reports & Analytics]
    
    %% User Management Branch
    F --> F1[View Users]
    F --> F2[Edit User]
    F --> F3[Delete User]
    F --> F4[Block User]
    F --> F5[Assign Roles]
    F --> F6[Reset Password]
    
    %% Content Management Branch
    G --> G1[Symptom Management]
    G --> G2[Disease Management]
    G --> G3[Test Management]
    G --> G4[Treatment Management]
    G --> G5[Education Content]
    G --> G6[Diagnostic Logic Engine]
    
    %% Symptom Management
    G1 --> G1A[Add/Edit/Delete Symptoms]
    G1 --> G1B[Set Symptom Severity]
    G1 --> G1C[Mark Required/Optional]
    G1 --> G1D[Bulk Import/Export]
    
    %% Disease Management
    G2 --> G2A[Add/Edit/Delete Diseases]
    G2 --> G2B[Map Symptoms to Diseases]
    G2 --> G2C[Attach Notes/References]
    G2 --> G2D[Link Diagnostic Logic]
    
    %% Test Management
    G3 --> G3A[Add/Edit/Delete Tests]
    G3 --> G3B[Set Test Units & Ranges]
    G3 --> G3C[Map Tests to Diseases]
    G3 --> G3D[Test Result Management]
    
    %% Diagnostic Logic Engine
    G6 --> G6A[Create/Edit Rule-based Logic]
    G6 --> G6B[AI/ML Integration]
    G6 --> G6C[Test Diagnostic Paths]
    
    %% Treatment Management
    G4 --> G4A[Add/Edit Treatment Protocols]
    G4 --> G4B[Map Treatments to Diseases]
    G4 --> G4C[Dosage & Duration Guidelines]
    G4 --> G4D[Link to Education Content]
    
    %% System Configuration
    H --> H1[Manage Roles & Permissions]
    H --> H2[Language/Localization]
    H --> H3[Theming Settings]
    H --> H4[System Maintenance]
    
    %% Reports & Analytics
    I --> I1[User Analytics]
    I --> I2[Disease Trends]
    I --> I3[System Activity Logs]
    I --> I4[Data Export]
    
    %% Styling
    classDef auth fill:#ffebee,stroke:#c62828,stroke-width:2px
    classDef dashboard fill:#e8f5e8,stroke:#2e7d32,stroke-width:3px
    classDef management fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    classDef content fill:#f3e5f5,stroke:#6a1b9a,stroke-width:2px
    classDef system fill:#fff8e1,stroke:#ef6c00,stroke-width:2px
    
    class A,B,D,E auth
    class C dashboard
    class F,F1,F2,F3,F4,F5,F6 management
    class G,G1,G2,G3,G4,G5,G6,G1A,G1B,G1C,G1D,G2A,G2B,G2C,G2D,G3A,G3B,G3C,G3D,G4A,G4B,G4C,G4D,G6A,G6B,G6C content
    class H,H1,H2,H3,H4,I,I1,I2,I3,I4 system
```

### 2. Diagnostic Logic Engine Flow
```mermaid
graph TD
    A[Diagnostic Logic Engine] --> B[Rule Management]
    A --> C[AI/ML Integration]
    A --> D[Testing & Validation]
    
    B --> B1[Create New Rule]
    B --> B2[Edit Existing Rule]
    B --> B3[Delete Rule]
    B --> B4[Rule Prioritization]
    
    B1 --> B1A[Define Conditions]
    B1A --> B1B[Set Symptoms Criteria]
    B1B --> B1C[Set Test Results Criteria]
    B1C --> B1D[Define Actions/Outcomes]
    B1D --> B1E[Set Confidence Level]
    
    C --> C1[Model Training]
    C --> C2[Feature Engineering]
    C --> C3[Model Validation]
    C --> C4[Deployment]
    
    D --> D1[Test Individual Rules]
    D --> D2[Test Complete Diagnostic Path]
    D --> D3[Validate Against Known Cases]
    D --> D4[Performance Metrics]
    
    D4 --> D4A[Accuracy Rate]
    D4 --> D4B[False Positive Rate]
    D4 --> D4C[False Negative Rate]
    D4 --> D4D[Response Time]
    
    %% Styling
    classDef engine fill:#e8f5e8,stroke:#2e7d32,stroke-width:3px
    classDef rules fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    classDef ai fill:#f3e5f5,stroke:#6a1b9a,stroke-width:2px
    classDef testing fill:#fff3e0,stroke:#ef6c00,stroke-width:2px
    
    class A engine
    class B,B1,B2,B3,B4,B1A,B1B,B1C,B1D,B1E rules
    class C,C1,C2,C3,C4 ai
    class D,D1,D2,D3,D4,D4A,D4B,D4C,D4D testing
```

## System Architecture Flow

### 1. Complete System Architecture
```mermaid
graph TB
    subgraph "User Interface Layer"
        A[Mobile App]
        B[Admin Panel]
        C[Web Portal]
    end
    
    subgraph "API Gateway"
        D[Authentication Service]
        E[API Router]
        F[Rate Limiting]
        G[Load Balancer]
    end
    
    subgraph "Business Logic Layer"
        H[User Management Service]
        I[Diagnostic Engine]
        J[Content Management Service]
        K[Analytics Service]
        L[Notification Service]
    end
    
    subgraph "Data Layer"
        M[(User Database)]
        N[(Medical Database)]
        O[(Analytics Database)]
        P[(File Storage)]
        Q[(Cache Layer)]
    end
    
    subgraph "External Services"
        R[Email Service]
        S[SMS Service]
        T[Push Notification Service]
        U[Medical APIs]
        V[AI/ML Services]
    end
    
    %% Connections
    A --> D
    B --> D
    C --> D
    
    D --> E
    E --> F
    F --> G
    
    G --> H
    G --> I
    G --> J
    G --> K
    G --> L
    
    H --> M
    I --> N
    I --> V
    J --> N
    J --> P
    K --> O
    L --> R
    L --> S
    L --> T
    
    I --> U
    H --> Q
    K --> Q
    
    %% Styling
    classDef ui fill:#e1f5fe,stroke:#0277bd,stroke-width:2px
    classDef api fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px
    classDef business fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    classDef data fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px
    classDef external fill:#ffebee,stroke:#c62828,stroke-width:2px
    
    class A,B,C ui
    class D,E,F,G api
    class H,I,J,K,L business
    class M,N,O,P,Q data
    class R,S,T,U,V external
```

### 2. Data Flow Diagram
```mermaid
graph LR
    A[User Input] --> B[Mobile App]
    B --> C[API Gateway]
    C --> D[Authentication]
    D --> E[Diagnostic Engine]
    
    E --> F[Symptom Analysis]
    F --> G[Rule Engine]
    G --> H[AI/ML Processing]
    H --> I[Diagnosis Generation]
    
    I --> J[Treatment Recommendations]
    J --> K[Educational Content]
    K --> L[Result Formatting]
    L --> M[Response to User]
    
    %% Data Storage
    E --> N[(Medical Database)]
    I --> O[(User Reports)]
    J --> P[(Treatment Database)]
    K --> Q[(Content Database)]
    
    %% Admin Flow
    R[Admin Input] --> S[Admin Panel]
    S --> C
    C --> T[Content Management]
    T --> N
    T --> P
    T --> Q
    
    %% Analytics
    E --> U[Analytics Service]
    U --> V[(Analytics Database)]
    V --> W[Dashboard Reports]
    
    %% Styling
    classDef userFlow fill:#e1f5fe,stroke:#0277bd,stroke-width:2px
    classDef processing fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px
    classDef storage fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px
    classDef admin fill:#fff3e0,stroke:#f57c00,stroke-width:2px
    
    class A,B,M userFlow
    class C,D,E,F,G,H,I,J,K,L processing
    class N,O,P,Q,V storage
    class R,S,T,U,W admin
```

## How to Use These Visual Flowcharts

### 1. **Mermaid Live Editor**
Copy any of the mermaid code blocks above and paste them into:
- [Mermaid Live Editor](https://mermaid.live/)
- GitHub (supports Mermaid in README files)
- GitLab (supports Mermaid in markdown)

### 2. **AI Diagramming Tools**
You can use these with AI tools like:
- **Lucidchart AI**
- **Draw.io (now Diagrams.net)**
- **Figma with AI plugins**
- **Whimsical**

### 3. **Development Tools**
- **VS Code** with Mermaid extensions
- **Notion** (supports Mermaid)
- **Confluence** (supports Mermaid)
- **Slack** (supports Mermaid)

### 4. **Export Options**
These diagrams can be exported as:
- **PNG/SVG** images
- **PDF** documents
- **Interactive HTML**
- **Editable formats** for further customization

The visual flowcharts include:
- ✅ **Color-coded sections** for easy navigation
- ✅ **Interactive decision points** 
- ✅ **Detailed process flows**
- ✅ **System architecture views**
- ✅ **Data flow representations**

These can be directly rendered as beautiful, professional diagrams using any Mermaid-compatible tool or AI diagramming service!