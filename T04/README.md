

---

# T04 · Servidor d’Impressió amb Printer Pooling

[solucio de la tasca](solucio.md)

## 📌 Introducció

En el sector logístic, la impressió continua sent un element crític: albarans, fulls de transport i documentació operativa han d’estar disponibles de manera immediata. FoodLogístic S.A. no és una excepció.

L’empresa disposa d’un magatzem on el volum d’impressió és molt elevat. Qualsevol fallada en una impressora pot bloquejar la sortida de camions i comprometre la cadena de fred. Per evitar-ho, cal implementar un **Servidor d’Impressió a Windows Server** amb **Printer Pooling**, permetent repartir la càrrega entre dues impressores virtuals.

Aquesta activitat consisteix a desplegar i documentar tota la infraestructura necessària, com si fos un **informe tècnic real per a un client**.

---

# 🧭 Descripció de l’activitat

El servidor ha de tenir:

- **Active Directory** per gestionar usuaris, equips i permisos.
- **Print Server** per centralitzar i controlar els recursos d’impressió.
- Un client Windows 11 integrat al domini, capaç d’autenticar-se i rebre la impressora de manera automatitzada.

La documentació ha de ser clara, estructurada i justificar totes les decisions tècniques.

L’activitat es divideix en quatre fases.

---

# 🟦 Fase 1: Preparació de l’entorn i simulació de maquinari

### ✔️ Tasques a realitzar

- Verificar o preparar l’entorn de Windows Server i Windows 11.
- Instal·lar **dues instàncies d’impressora PDF24** al servidor (segons la guia proporcionada).
- Assignar noms corporatius:
  - `IMP_MAGATZEM_A`
  - `IMP_MAGATZEM_B`

Aquestes impressores actuaran com a dispositius físics en un entorn real.

---

# 🟦 Fase 2: Instal·lació del Rol i Configuració del Pool

### ✔️ Instal·lació del rol

- Instal·lar **Print and Document Services** al Windows Server.
- Obrir la consola **Print Management**.

### ✔️ Configuració del Printer Pooling

1. Obrir les propietats de `IMP_MAGATZEM_A`.
2. A la pestanya **Ports**, activar:
   - **Enable printer pooling**
3. Seleccionar també el port utilitzat per `IMP_MAGATZEM_B`.
4. Confirmar que **a `IMP_MAGATZEM_A` queden seleccionats els dos ports virtuals**.

A partir d’aquest moment, les dues impressores funcionen com una sola cua de xarxa, repartint automàticament la càrrega.

---

# 🟦 Fase 3: Desplegament automatitzat amb GPO

L’empresa no vol que els treballadors del magatzem instal·lin manualment la impressora.

### ✔️ Tasques a realitzar

- Crear una GPO anomenada **`GPO_Impressores_Magatzem`**.
- Des de Print Management, utilitzar **Deploy with Group Policy**.
- Vincular la impressora al domini o a una OU específica.
- Iniciar sessió al client Windows 11 i verificar que la impressora apareix automàticament.

### Nota tècnica

- Pot ser necessari tancar sessió o executar:

```
gpupdate /force
```

---

# 🟦 Fase 4: Prova de càrrega i Seguretat

### ✔️ Simulació de balanceig

- Enviar **10 documents consecutius** a la impressora del magatzem.
- Observar com el servidor distribueix les impressions entre les dues instàncies.

### ✔️ Restriccions i polítiques

Configurar:

- **Printing Priorities**  
  o bé  
- **Available Times**

Per exemple, limitar l’ús de la impressora a l’horari laboral:

- De **06:00** a **22:00**

Això garanteix control i seguretat en l’ús del recurs.

---

# 📚 Material de suport

- **0224 SOX – Material UD8: AA3** (Moodle de l’assignatura)
- **Guia tècnica:** Instal·lació i configuració de PDF24

---

Si vols, puc ajudar-te a:

- Convertir aquest README en un **informe tècnic complet** amb captures i explicacions detallades.
- Crear una **plantilla d’informe professional** per entregar al professorat.
- Redactar la justificació tècnica de cada decisió (per què AD, per què GPO, per què pooling, etc.).

Només digues com vols continuar.