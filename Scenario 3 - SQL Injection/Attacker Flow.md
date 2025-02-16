```mermaid
  sequenceDiagram
    participant Attacker
    participant SolariHealthApp
    participant CnCServer
    participant BackendServer
    participant User
    activate Attacker
    Attacker->>SolariHealthApp: Identify Solari Health 360 app
    SolariHealthApp->>Attacker: Application identified
    deactivate Attacker
    activate Attacker
    Attacker->>SolariHealthApp: Craft exploit for known vulnerabilities
    SolariHealthApp->>Attacker: Exploit crafted
    deactivate Attacker
    activate Attacker
    Attacker->>SolariHealthApp: Carry out SQL Injection via input fields 
    SolariHealthApp->>Attacker: Malicious SQL query is validated 
    BackendServer->>CnCServer: Communication established
    CnCServer->>BackendServer: Commands issued
    BackendServer->>CnCServer: Access Granted to View, Alter or Delete records.
    BackendServer->>CnCServer: Act as Database administrator 
    deactivate Attacker
