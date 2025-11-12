[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/56oe51os)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21609016&assignment_repo_type=AssignmentRepo)
# LV3 - statističko zaključivanje o dvjema varijablama

Ovaj repozitorij sadrži materijale i rješenja za laboratorijske vježbe iz područja statističkog zaključivanja dviju varijabli.
Vježba obuhvaća primjenu parametarskih i neparametarskih metoda za usporedbu uzoraka te analizu odnosa između dviju varijabli primjenom jednostavne linearne regresije.
Glavni naglasak je na analizi podataka, odabiru odgovarajućih statističkih metoda, vizualizaciji rezultata i interpretaciji dobivenih pokazatelja i koeficijenata.

# Koncept laboratorijske vježbe

Tijekom vježbe pokrivaju se sljedeće temeljne statističke metode i koncepti:

* Usporedba dvaju uzoraka (nezavisnih i zavisnih).
* Provjera pretpostavki:
    - normalnost distribucije pomoću Shapiro–Wilk testa,
    - homoskedastičnost varijanci pomoću Leveneovog testa.
* Odabir odgovarajućeg testa ovisno o pretpostavkama (npr. Pooled vs. Welch t-test, parametarske i neparametrijske alternative poput Mann–Whitney U i Wilcoxon signed-rank testa).
* Jednostavna linearna regresija i analiza odnosa između dvije varijable.
* Analiza reziduala za provjeru adekvatnosti i pretpostavke homoskedastičnosti modela.
* Interpretacija koeficijenta determinacije ($R^2$) kao mjere adekvatnosti modela.

# Zadaci za LV3 ( 2025./2026.)
U vježbi se koriste stvarni podaci iz CalCOFI baze (varijable: Depthm, T_degC, Salnty), osim u Zadatku 3, koji koristi priložene podatke prije/poslije intervencije (ispitanici.xlsx).

## Zadatak 1: Statističko zaključivanje o temperaturi u dvjema dubinskim zonama (Nezavisni uzorci)

**Cilj:** Ispitati postoji li statistički značajna razlika u temperaturi mora (T_degC) između površinskog sloja (Depthm < 50 m) i dubljeg sloja (Depthm > 200 m).

Koraci:

1. Podjela i uzorkovanje podataka (korištenje uzorka od 5000 slučajnih vrijednosti).
2. Ispitivanje normalnosti distribucije (Shapiro–Wilk test) i jednakosti varijanci (Leveneov test).
3. Odabir testa (t-test za nezavisne uzorke ili Mann–Whitney U test) ovisno o zadovoljenju pretpostavki.
4. Testiranje hipoteze $H_0: \mu_{pliće} = \mu_{dublje}$ i interpretacija rezultata.

## Zadatak 2: Jednostavna linearna regresija (Temperatura – Dubina)

**Cilj:** Modelirati ovisnost temperature (T_degC) o dubini mora (Depthm) pomoću jednostavne linearne regresije.

Koraci:

1. Priprema podataka: Uklanjanje ekstremnih ili nerealnih vrijednosti primjenom fizički smislenih raspona i IQR metode.
2. Vizualizacija: Izrada scatter dijagrama (Depthm – T_degC).
3. Procjena modela $T_{degC} = \beta_0 + \beta_1 \times Depthm + \varepsilon$ koristeći funkciju linregress().
4. Izračun i interpretacija koeficijenata ($\beta_0$, $\beta_1$), koeficijenta korelacije ($r$) i determinacije ($R^2$), te p-vrijednosti za nagib.
5. Analiza reziduala (vizualno i statistički) radi provjere homoskedastičnosti i adekvatnosti modela.

## Zadatak 3: Usporedba rezultata prije i poslije intervencije (Zavisni uzorci)

**Cilj:** Provjeriti postoji li statistički značajna razlika između rezultata testova prije (Pre) i nakon (Post) provođenja specifičnog programa ili intervencije.

Koraci:

1. Deskriptivna statistika rezultata prije i poslije (sredina, medijan, kvartili, standardna devijacija).
2. Odabir metode:
    - provjera normalnosti razlika (Shapiro–Wilk test),
    - odabir između parnog t-testa (ako su razlike normalne) i Wilcoxonovog testa s predznakom (ako nisu).
3. Vizualizacija: prikaz podataka pomoću boxplot dijagrama i histograma razlika.
4. Interpretacija: pisanje kratkog izvještaja s p-vrijednošću, razinom značajnosti ($\alpha$) i zaključkom o postojanju značajne razlike.
