# Raport Początkowy

**Autor:** Aleksander Śmiałowski  
**Temat:** Prognozowanie Obciążenia Krajowego Systemu Elektroenergetycznego (KSE) wraz z analizą trendów sezonowych.

---

## Definicja problemu

Energia elektryczna stanowi kręgosłup nowoczesnej gospodarki. W dobie transformacji energetycznej, precyzyjne prognozowanie zapotrzebowania na moc w Krajowym Systemie Elektroenergetycznym (KSE) stało się krytycznym wyzwaniem dla stabilności sieci i bezpieczeństwa energetycznego kraju.

### Problem badawczy
Jak skutecznie przewidzieć zapotrzebowanie na energię z wyprzedzeniem tygodniowym, uwzględniając złożone cykle dobowe, tygodniowe oraz specyfikę dni ustawowo wolnych od pracy.

### Cele projektu
* **Analiza wzorców:** Identyfikacja historycznych wzorców zużycia energii w Polsce w krytycznym okresie grzewczym i świątecznym (połowa listopada 2025 - koniec stycznia 2026).
* **Badanie trendu:** Zrozumienie dynamiki zmian zapotrzebowania w zależności od typu dnia (roboczy vs wolny) oraz pory doby.

---

## Metodologia i Technologia

Do realizacji projektu wybrano bibliotekę **Facebook Prophet**. Jest to nowoczesne narzędzie statystyczne zorientowane na szeregi czasowe o silnej sezonowości, które natywnie obsługuje kalendarze świąt, co jest kluczowe dla analizy okresu grudniowego.

---

## Hipotezy Badawcze

* **H1 (Sezonowość):** Zużycie energii wykazuje podwójną sezonowość: dobową (szczyty poranne i wieczorne) oraz tygodniową.
* **H2 (Obsługa anomalii):** Model Facebook Prophet skutecznie zneutralizuje wpływ dni wolnych od pracy na jakość prognozy dzięki wbudowanej bazie świąt.
* **H3 (Dokładność):** Średni błąd procentowy (MAPE) modelu nie przekroczy progu 5%.

---

## Dane wejściowe

* **Źródło:** Oficjalne dane operacyjne Polskich Sieci Elektroenergetycznych (PSE).
* **Zmienna objaśniana:** Rzeczywiste zapotrzebowanie KSE [MW].
* **Zakres:** 17.11.2025 - 25.01.2026 (dane godzinowe).
