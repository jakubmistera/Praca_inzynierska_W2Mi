# Aplikacja do sterowania zgrzewarką tarciową W2Mi

Projekt inżynierski obejmujący kompleksowe oprogramowanie układu sterowania maszyny do zgrzewania tarciowego materiałów ultradrobnoziarnistych (UFG). System oparty jest na środowisku i komponentach firmy Mitsubishi Electric.

## 🛠 Wykorzystany sprzęt (Hardware)
* **Sterownik PLC:** Mitsubishi FX5U-32M
* **Moduł pozycjonowania (Simple Motion):** FX5-40SSC-S
* **Serwowzmacniacz:** MR-JE-100BF
* **Falownik:** GD10-2RZG-S2-B
* **Panel HMI:** GS2107-WTBD-N

## 💻 Środowisko programistyczne i technologie
* **GX Works3:** Główna logika programu napisana w języku **FBD/LD** z wykorzystaniem biblioteki **PLCOpen** (bloki sterowania ruchem m.in. `MC_Power`, `MC_Home`, `MC_MoveAbsolute`).
* **GT Designer3:** Projektowanie i konfiguracja interfejsu graficznego (HMI).
* **MR Configurator2:** Konfiguracja parametrów serwowzmacniacza (elektroniczna przekładnia, limity prędkości).
* **Komunikacja:** Konfiguracja wyjść analogowych (0-10V) do sterowania częstotliwością falownika.

## ⚙️ Główne funkcjonalności programu
Projekt dzieli się na 4 główne moduły operacyjne, zarządzane z poziomu panelu HMI:
1. **Sterowanie ręczne (JOG):** Ręczny przejazd próbki z wykorzystaniem zadanej prędkości i kierunku.
2. **Bazowanie (Homing):** Procedura bazowania stałym momentem obrotowym (Data Set Method), zapewniająca stałą odległość między czołami elementów niezależnie od ich długości początkowej.
3. **Sterowanie falownikiem:** Regulacja prędkości obrotowej elektrowrzeciona (0-400 Hz) za pomocą sygnału analogowego wraz z monitorowaniem aktualnej prędkości.
4. **Nastawa parametrów i praca automatyczna:** Automatyczny cykl dojazdu próbek z wykorzystaniem różnych prędkości (szybki dojazd, wolniejsze zagłębianie/tarcie) z użyciem bloków `MC_MoveRelative`.

## 📷 Prezentacja logiki i HMI (fragmenty)

### Uruchomienie osi
<img width="851" height="333" alt="image" src="https://github.com/user-attachments/assets/95abd8e7-2d14-44aa-85cb-cb3e206ee49a" />

### Bazowanie
<img width="1215" height="313" alt="image" src="https://github.com/user-attachments/assets/0a200063-974a-4fc4-b0a1-eae8ae018116" />

### Dojazd
<img width="1343" height="264" alt="image" src="https://github.com/user-attachments/assets/aab5a7e4-9afc-423f-b97c-7294d9ef47c5" />

### HMI - Bazowanie
<img width="992" height="590" alt="image" src="https://github.com/user-attachments/assets/e72f1a06-fe10-46cf-8162-a9513527c82f" />

### HMI - Nastawa parametrów
<img width="990" height="586" alt="image" src="https://github.com/user-attachments/assets/97c5e050-e5be-458e-bfb0-29b2f87eab80" />

---
*Projekt zrealizowany w ramach pracy inżynierskiej na Politechnice Warszawskiej (Kierunek: Automatyzacja i Robotyzacja Procesów Produkcyjnych).*
