@startuml
skinparam state {
  BackgroundColor<<godkant>> #EAF3DE
  BorderColor<<godkant>> #3B6D11
  FontColor<<godkant>> #173404

  BackgroundColor<<nekat>> #FCEBEB
  BorderColor<<nekat>> #A32D2D
  FontColor<<nekat>> #501313

  BackgroundColor<<neutral>> #F1EFE8
  BorderColor<<neutral>> #5F5E5A
  FontColor<<neutral>> #2C2C2A
}

state "Ejhanterat" as Ejhanterat <<neutral>>
state "Godkänt" as Godkant <<godkant>>
state "Nekat" as Nekat <<nekat>>

[*] --> Ejhanterat

Ejhanterat --> Godkant : Godkänner samtycke
Ejhanterat --> Nekat : Nekar samtycke

Godkant --> Nekat : Ändrar val till nekat
Nekat --> Godkant : Ändrar val till godkänt

Godkant ..> Ejhanterat : Rensar cookies
Nekat ..> Ejhanterat : Rensar cookies
@enduml
