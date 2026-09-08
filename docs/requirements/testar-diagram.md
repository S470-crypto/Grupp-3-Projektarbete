
```mermaid
flowchart TD
    Start(( )) --> E[Ejhanterat]


E -->|Godkänner samtycke| G[Godkänt]
E -->|Nekar samtycke| N[Nekat]

G -->|Rensar cookies| E
N -->|Rensar cookies| E

G -->|Ändrar val till nekat| N
N -->|Ändrar val till godkänt| G

%% Osynlig nod för att skapa mer horisontellt utrymme
G ~~~ Spacer[ ]
Spacer ~~~ N

style E fill:#f0eee7,stroke:#aaa,color:#444
style G fill:#e8f4dc,stroke:#8caf6c,color:#285b1c
style N fill:#fce8e8,stroke:#d77b7b,color:#8b2929
style Spacer fill:none,stroke:none,color:none
