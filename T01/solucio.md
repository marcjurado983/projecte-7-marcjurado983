#️⃣ Fase 1 — Coneixent el terreny i la competència
## Context inicial
Hem creat una empresa de serveis informàtics amb seu a Mataró, per donar servei a empreses del Maresme.
El primer gran client potencial és FoodLogístic S.A., empresa de logística alimentària al polígon de les Hortes del Camí Ral, que necessita una renovació integral de la seva infraestructura tecnològica.

Abans de definir pressupostos i preus/hora, cal entendre:

Com funciona el sector

Quins serveis s’ofereixen habitualment

Qui són els competidors directes a la zona

## 1. Recerca de mercat: competència al Maresme
A continuació es presenten 3 empreses reals de serveis informàtics que operen a Mataró o rodalies.

### 1.1 Digitalnet (Mataró)
Mida: PIME
Ubicació: Mataró

Serveis principals:

Manteniment informàtic per empreses

Servidors i xarxes

Còpies de seguretat i serveis cloud

Hardware i solucions d’impressió

Perfil competitiu:  
Empresa consolidada amb molts anys d’experiència i enfocament a empreses locals.

### 1.2 JSM Consultoria Tecnològica (Mataró)
Mida: PIME mitjana
Ubicació: Mataró (àmbit Catalunya)

Serveis principals:

Serveis Cloud professionals

Ciberseguretat

Xarxes corporatives i WiFi professional

Programari de gestió (ERP, Sage)

Perfil competitiu:  
Empresa molt especialitzada, orientada a serveis integrals i empreses mitjanes.

### 1.3 Serveis Informàtics Maresme (Arenys de Munt)
Mida: microempresa / PIME petita
Ubicació: Arenys de Munt (servei a tot el Maresme)

Serveis principals:

Suport tècnic presencial i remot

Xarxes i WiFi

Recuperació de dades

Assessorament tecnològic

Perfil competitiu:  
Proximitat, tracte personal i flexibilitat.

## 2. Organigrama de l’empresa tipus (model de competència)
S’ha definit una estructura organitzativa mitjana, representativa d’una PIME de serveis informàtics del Maresme.

### 2.1 Estructura jeràrquica
Codi
Direcció
├── Departament Tècnic
│   ├── Sistemes i Xarxes
│   └── Suport i Helpdesk
├── Departament Comercial
└── Administració i Gestió
### 2.2 Organigrama amb PlantUML
plantuml
@startuml
title Organigrama empresa de serveis informàtics (PIME)

class Direccio {
CEO / Gerència
}

class Tecnic {
Responsable Tècnic
}

class Sistemes {
Sistemes i Xarxes
}

class Helpdesk {
Suport i Helpdesk
}

class Comercial {
Comercial
}

class Administracio {
Administració
}

Direccio --> Tecnic
Direccio --> Comercial
Direccio --> Administracio

Tecnic --> Sistemes
Tecnic --> Helpdesk

@enduml
Aquest codi es pot copiar directament a PlantUML i genera un organigrama coherent i realista.

## 3. Radiografia de departaments
### Direcció / Gerència
Presa de decisions estratègiques

Relació amb clients clau

Definició de preus, serveis i aliances

### Departament Tècnic
Funció principal: garantir el funcionament correcte de totes les infraestructures IT dels clients.

Sistemes i Xarxes
Servidors, backups, xarxes, VLAN, seguretat

Instal·lació i manteniment preventiu

Suport / Helpdesk
Resolució d’incidències

Assistència remota i presencial

Gestió de tickets i SLA

### Departament Comercial
Captació de nous clients

Elaboració de propostes tècniques i pressupostos

Seguiment comercial i fidelització

### Administració
Facturació i cobraments

Gestió de proveïdors

Aspectes legals, contractes i documentació

#️⃣ Fase 2 — Estratègia
## 4. Definició de la nostra estratègia (proposta de valor)
Per diferenciar-nos de la competència i convèncer FoodLogístic S.A., la nostra proposta de valor es basa en:

Proximitat i rapidesa
Empresa local de Mataró

Temps de resposta molt curts

Especialització en logística alimentària
Coneixement de sistemes crítics

Traçabilitat

Còpies de seguretat

Continuïtat del servei

Servei integral
Un sol proveïdor per:

Sistemes

Xarxes

Suport

Ciberseguretat

Assessorament tecnològic

Monitorització i manteniment preventiu
Evitar problemes abans que afectin la producció

## 5. Recursos necessaris per donar servei a FoodLogístic S.A.
Recursos humans inicials
1 tècnic de sistemes i xarxes

1 tècnic de suport / helpdesk

1 responsable de projecte / direcció

Valoració
Per a una empresa mitjana com FoodLogístic:

Inicialment és suficient aquest equip

En cas de creixement o servei 24/7 → caldria contractar un segon tècnic de suport

Permet escalar el servei sense perdre qualitat ni proximitat

## Conclusió
El sector dels serveis informàtics a Mataró està format principalment per PIMEs amb estructures similars, fet que obliga a competir no només en preu, sinó en:

Qualitat

Especialització

Tracte directe

La nostra estratègia se centra en:

Coneixement del client

Servei personalitzat

Fiabilitat

Relació a llarg termini

Aquesta combinació ens posiciona com una opció realment competitiva davant FoodLogístic S.A.