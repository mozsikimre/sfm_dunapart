# 🚗 Parkolókezelő Webalkalmazás

Egy teljes stackes webalkalmazás, amely egy digitális parkolókezelő rendszerként szolgál. A projekt célja, hogy a felhasználók regisztrálhassanak, autókat adhassanak hozzá saját garázsukhoz, és valós idejű parkolóhelyeket foglalhassanak autóik mérete alapján egy háromszintes parkolóházban.

## 🔧 Technológiai Stack

- **Frontend**: React, JSX
- **Backend**: Java, Spring Boot
- **Adatbázis**: Beépített H2

## 🌐 Funkcionalitás

### 🏠 Kezdőoldal
- Üdvözlő képernyő felhasználók számára.
- Megjelennek a felhasználóhoz tartozó autók (ha van aktív parkolásuk).
- Autó hozzáadása gomb.
- Parkolások törlése / hosszabbítása gombok.
- Bejelentkezés / Kijelentkezés gomb a fejlécben.
- 🌙 Sötét/Világos mód kapcsoló (helyileg mentve a `localStorage`-ben).

### 🔐 Autentikáció
- Regisztráció és bejelentkezés.
- Elfelejtett jelszó opció (demó módban működik – közvetlen jelszócsere üzenetküldés nélkül).

### 🚙 Garázs / Autóválasztó
- A felhasználó autóinak listája kártyás formában.
- Kártyán megjelenített adatok: típushoz tartozó stock kép, autó neve, rendszám, típus és szín.
- Autó hozzáadása gomb.
- Autó törlése / szerkesztése gomb.
- Aktív autó kiválasztásának lehetősége.

### 🗓️ Időpont Foglaló
- Csak aktív autó esetén használható.
- Naptár alapú időintervallum kiválasztása (nap, óra, perc pontossággal).
- Foglalás mentése és továbbnavigálás a parkoló nézetre.

### 🅿️ Parkoló Oldal
- 3 szintes parkolóház vizualizációja.
- Emeletváltás 3 gomb segítségével.
- Parkolóhelyek megjelenítése méret és foglaltság alapján:
  - 🔴 Nem kompatibilis vagy foglalt hely
  - ⚪ Szabad, választható hely
  - 🟢 Foglalt saját hely
  - 🟡 Hamarosan felszabaduló hely
- Tooltip információ a parkolóhelyek felett: autó neve és foglalási időintervallum.
- Parkolóhelyek és járművek méret-ellenőrzése.

### 🧭 Navigációs Sáv
- Drag & drop funkcióval mozgatható navigációs panel.
- Mágneses igazítás az oldal széléhez.
- Összecsukható nyíl a felső részén.
- Navigációs elemek:
  - Kezdőlap
  - Autentikáció
  - Garázs
  - Időpont foglaló
  - Parkoló

## 🎨 Design
- Modern, reszponzív felület.
- Fő színséma: **zöld és narancssárga**.
- 🌙 Világos/sötét mód közötti váltás lehetősége.

## 💡 Megjegyzés
Ez a projekt egy technikai bemutató céljára készült, így bizonyos funkciók (pl. jelszó visszaállítás) nem teljes értékűek.

---

## 🚀 Telepítés

### Backend (Spring Boot)
1. Navigálj a `backend/` könyvtárba.
2. Indítsd el az alkalmazást:
```bash
./mvnw spring-boot:run
