# T01: Coneixent la competència i el sector**

![coneixent](img/img.png.png)

MARC JURADO I MARTI CODONY

# Fase 1 Coneixent el terreny i la competència**

1\. Recerca de mercat (3 empreses reals del Maresme)

tres empreses reals de serveis informàtics que operen a Mataró i rodalies

1.informático Mataró  

**Mida:** Microempresa

**Serveis:** Reparació d’ordinadors, manteniment informàtic, suport a domicili, xarxes, servidors, seguretat, backup, monitorització.

[https://www.informaticomataro.com/?utm\_source=copilot.com](https://www.informaticomataro.com/?utm_source=copilot.com)

2.Sisticat (Tecnologia i Desenvolupament de Sistemes SL)

**Mida:** PIME

**Serveis:** Servei tècnic per empreses, hosting, dominis, correu, xarxes, servidors, 

[Sisticat – Serveis tecnològics a Mataró, Maresme i Barcelonahttps://](https://sisticat.cat/?utm_source=copilot.com)[sisticat.cat/](http://sisticat.cat/)

3.JSM Consultoria Tecnològica

Mida: PIME

Serveis: Manteniment informàtic, serveis cloud, software de gestió, ciberseguretat, xarxes, 

[Servicios informática Mataró y Barcelona | JSM Inforedeshttps://](https://jsm-consultoria-tecnologica.es/?utm_source=copilot.com)[jsm-consultoria-tecnologica.es/](http://jsm-consultoria-tecnologica.es/)

2\. Organigrama (empresa tipus basada en la competència)

HeM creat un organigrama realista basat en una PIME tecnològica del Maresme

Organigrama en PlantUML \+ UMLTree

@startuml  
skinparam defaultTextAlignment center  
skinparam rectangle {  
  BackgroundColor \#E8F0FE  
  BorderColor \#2C3E50  
}

rectangle "Direcció General" as DG {  
}

rectangle "Departament Tècnic" as DT {  
}

rectangle "Departament de Sistemes" as DS {  
}

rectangle "Helpdesk / Suport" as HD {  
}

rectangle "Departament Comercial" as DC {  
}

rectangle "Administració" as ADM {  
}

DG \--\> DT  
DG \--\> DC  
DG \--\> ADM  
DT \--\> DS  
DT \--\> HD

@enduml

Versió UMLTree (estructura jeràrquica)

Direcció General  
├── Departament Tècnic  
│   ├── Sistemes  
│   └── Helpdesk / Suport  
├── Departament Comercial  
└── Administració

3\. Radiografia de departaments

Tenim la direccio General de la estructura amb la gestió global de la empresa i tenint una estrategia, amb bones desicions i coordinació de departaments.

Despres tenim el Departament tecnic amb la coordinació dels projectes IT i la supervisió de sistemes i xarxes

A continuació tenim els sistemes lligats amb el departament tecnic amb administració de servidors, xarxes i infraestructura, tambe copies de seguretat i virtualització

també el helpdesk /suport atencio a incidencies i suport remot

Comercial voler captar la atenció dels clients, tenir pressupostos i bons contactes

I finalment la administració amb facturació i comptabilitat, recursos humans RRHH i contractació

# FASE 2 — Estratègia

1\. Proposta de valor (diferenciació)**

la nostra empresa volem que destaci

amb la nostra proposta de valor que donem

\-poder donar proximitat i una resposta rapida menys de 4 hores  
\-Servei personalitzat com tracte directe  
\-preus transparents i plans modulars  
\-moniorització proactiva per no tenir ninguna incidencia

avui en dia per donar competitivitat al maresme el millor es proximitat, confiança i rapidesa

2\. Recursos humans necessaris**

Si som una empresa per donar un servei basic per poder competir amb PIME el el sector el millor equip recomenat nostre és

| Rol | persones | Funcions |
| ----- | ----- | ----- |
| Tècnic de Sistemes | 1 | Servidors, xarxes, seguretat |
| Tècnic Helpdesk | 1 | Suport i incidències |
| Comercial | 0.5 (pot ser compartit) | Captació i seguiment |
| Administració | 0.25 (externalitzable) | Facturació i gestió |

Conclusió

Amb 1 persona no n’hi ha prou per competir amb empreses com Sisticat o JSM.

Amb 2 persones pots començar, però necessitem externalitzar administració i reforçar suport.

Amb 3 persones ja podem oferir un servei estable i competitiu.
