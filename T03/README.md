

---

# T03 — Servidor de Fitxers

## 📌 Introducció
Quan el volum de negoci creix, també ho fa el volum de dades, i sovint això comporta problemes d’organització i visibilitat. FoodLogistic no n’ha estat una excepció: cada departament guardava la documentació de forma local, dificultant la gestió centralitzada.

L’objectiu d’aquesta activitat és implementar una infraestructura de fitxers segura, organitzada i amb control d’espai, utilitzant:

- Permisos **NTFS/SMB**
- **Quotes NTFS**
- **FSRM** (File Server Resource Manager)
- Tres vies d’administració: **Explorador de fitxers**, **Server Manager** i **PowerShell**

---

## 🧩 Descripció de l’activitat
L’activitat es divideix en fites que simulen un procés real de consultoria i implementació.

---

## 1️⃣ Preparació i Seguretat de Grups (Active Directory)

Abans de crear el servidor de fitxers, cal preparar l’estructura d’Active Directory sobre el domini `foodlogistic.test`.

Es recomana crear una estructura d’**OUs coherent**, justificada segons les necessitats del projecte.

### ✔️ Grups de seguretat a crear
| Grup | Funció |
|------|--------|
| **Administracio** | Gestió de factures i albarans |
| **Transport** | Xofers i caps de flota |
| **Direccio** | Gerència |

---

## 2️⃣ Implementació de Recursos Compartits (3 mètodes)

Heu de crear les carpetes següents, cadascuna amb un mètode diferent.

---

### **A. Carpeta `Public` (Mètode: Explorador d’Arxius)**

- Compartida per a tothom.
- **Permisos SMB:** Lectura  
- **Permisos NTFS:** Modificació  
- Verificar la combinació de permisos efectiva.

---

### **B. Carpeta `Operacions` (Mètode: Server Manager — FSSM)**

1. Instal·lar el rol **File and Storage Services** si no hi és.
2. Crear el recurs compartit.
3. Activar **Access-Based Enumeration**.
4. **Restricció:** només el grup *Transport* hi pot accedir.

---

### **C. Carpeta `Direccio$` (Mètode: PowerShell bàsic)**

- Crear la carpeta oculta `Direccio$`.
- **Accés exclusiu:** grup *Direccio*.
- Compartir-la amb `New-SmbShare`.
- Crear una **GPO** perquè aparegui com a unitat `Z:` només per als usuaris de Direcció.

---

### **D. Carpeta `Direccio` (Mètode: PowerShell avançat)**  
*(Opcional, però amb més valoració)*

- Crear la carpeta `Direccio`.
- **Accés exclusiu:** grup *Direccio*.
- Compartir-la amb `New-SmbShare`.
- Activar **Access-Based Enumeration** via PowerShell.
- Crear una **GPO** perquè aparegui com a unitat `Z:` només per Direcció.

> Cal triar entre el mètode **C** o **D** (el D puntua més).

---

## 3️⃣ Control d’Emmagatzematge (FSRM i Quotes NTFS)

El client es queixa que els usuaris omplen el disc amb fotos personals. Cal aplicar controls.

---

### **Quotes NTFS (Control per Volum)**

- Activar quotes NTFS a la unitat de dades.
- Establir un límit per defecte de **500 MB** per a qualsevol usuari nou.

---

### **FSRM (Control per Carpeta)**

#### 📁 Quota de Carpeta (Public)
- Aplicar una quota **Hard** de **200 MB**.
- Avis al 90% amb el missatge:
  > *"Compte! FoodLogístic t'informa que estàs a punt d'esgotar l'espai compartit."*

#### 🚫 Filtrat de Fitxers (Operacions)
- Impedir guardar:
  - `.exe`
  - `.msi`
  - Fitxers d’àudio
  - Fitxers