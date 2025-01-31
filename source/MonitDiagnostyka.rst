Monitorowanie i Diagnostyka
===========================
:Author: - Kajetan Parka
	 - Mikołaj Piłat

1. **Sesje i użytkownicy**: Monitorowanie sesji i użytkowników w administracji baz danych jest kluczowym elementem. Pozwala to na śledzenie aktywności użytkowników, zarządzanie zasobami oraz wykrywanie potencjalnych problemów.

	1.1 **Szczegółowe monitorowanie aktywności użytkowników**: Administratorzy baz danych mogą śledzić, które zapytania są wykonywane przez użytkowników, jak długo trwają te zapytania i jakie są ich wyniki. Można to zrobić za pomocą narzędzi takich jak SQL Profiler (w przypadku SQL Server) lub AWR (w przypadku Oracle). Te narzędzia mogą dostarczyć szczegółowych informacji na temat zapytań, takich jak czas wykonania, zużycie procesora, ilość odczytów i zapisów na dysk, a nawet plan wykonania zapytania. Dodatkowo, administratorzy mogą monitorować aktywność na poziomie sesji, taką jak liczba otwartych transakcji, czas trwania sesji, używane zasoby i inne.

	1.2 **Zarządzanie zasobami na poziomie sesji**: Administratorzy baz danych mogą używać narzędzi do monitorowania zasobów, takich jak Performance Monitor (w przypadku Windows) lub top (w przypadku Linux), aby zobaczyć, które procesy zużywają najwięcej zasobów. Można również skonfigurować limity zasobów dla poszczególnych użytkowników lub sesji, aby zapobiec monopolizowaniu zasobów przez pojedyncze sesje. Administratorzy mogą również monitorować użycie zasobów na poziomie sesji, takie jak zużycie procesora, pamięci, dysku i sieci, co może pomóc w identyfikowaniu i rozwiązywaniu problemów z wydajnością.

	1.3 **Wykrywanie problemów na poziomie sesji**: Administratorzy baz danych mogą używać narzędzi do monitorowania bazy danych, aby wykrywać problemy takie jak blokady, długotrwałe transakcje, czy błędy w zapytaniach. Na przykład, SQL Server oferuje narzędzie o nazwie Activity Monitor, które pokazuje informacje o blokadach, a Oracle oferuje narzędzie o nazwie Automatic Database Diagnostic Monitor (ADDM), które automatycznie wykrywa i diagnozuje problemy z wydajnością. Administratorzy mogą również monitorować logi błędów i ostrzeżeń generowane przez DBMS, co może pomóc w identyfikowaniu i rozwiązywaniu problemów.

	1.4 **Bezpieczeństwo**: Monitorowanie sesji i użytkowników jest również ważne z punktu widzenia bezpieczeństwa. Administratorzy mogą śledzić, kto loguje się do systemu, kiedy to robią i co robią. Można to zrobić za pomocą logów audytu bazy danych. W przypadku podejrzanej aktywności, takiej jak próby logowania poza normalnymi godzinami pracy, administratorzy mogą podjąć odpowiednie działania, takie jak zmiana hasła użytkownika lub zablokowanie konta.

	1.5 **Zgodność**: Monitorowanie sesji i użytkowników jest również ważne z punktu widzenia zgodności z przepisami. Administratorzy mogą używać narzędzi do audytu, takich jak SQL Server Audit lub Oracle Database Audit, aby zobaczyć, kto miał dostęp do jakich danych i kiedy. Te informacje mogą być użyte do udowodnienia zgodności z przepisami dotyczącymi ochrony danych, takimi jak RODO.

2. **Śledzenie dostępu użytkowników do poszczególnych tabel**: Śledzenie dostępu użytkowników do poszczególnych tabel jest istotnym elementem monitorowania i diagnostyki bazy danych. Pozwala to na zrozumienie, jak użytkownicy korzystają z danych, a także na wykrywanie potencjalnych problemów lub podejrzanej aktywności.

	2.1 **Zrozumienie użycia danych**: Administratorzy baz danych mogą używać narzędzi do monitorowania dostępu do tabel, aby zrozumieć, jakie tabele są najczęściej odwiedzane i jakie operacje są najczęściej wykonywane. Na przykład, mogą używać narzędzi do monitorowania wydajności, takich jak SQL Server Profiler lub Oracle Enterprise Manager, aby zobaczyć, które zapytania są najczęściej wykonywane i jak długo trwają. Mogą również używać narzędzi do analizy logów, takich jak Log Miner w Oracle, aby zobaczyć, kiedy i przez kogo dane tabele były modyfikowane. Te narzędzia mogą dostarczyć szczegółowych informacji na temat zapytań, takich jak czas wykonania, zużycie procesora, ilość odczytów i zapisów na dysk, a nawet plan wykonania zapytania.

	2.2 **Wykrywanie problemów**: Jeśli użytkownik nagle zaczyna wykonywać dużą liczbę zapytań do określonej tabeli, może to być oznaką problemu. Na przykład, może to oznaczać, że zapytanie jest niewłaściwie skonstruowane lub że aplikacja jest zapętlona. Administratorzy mogą używać narzędzi do monitorowania wydajności, aby zidentyfikować te problemy i podjąć odpowiednie działania. Narzędzia te mogą dostarczyć szczegółowych informacji na temat zapytań, takich jak czas wykonania, zużycie procesora, ilość odczytów i zapisów na dysk, a nawet plan wykonania zapytania.

	2.3 **Bezpieczeństwo i zgodność**: Śledzenie dostępu do tabel jest również ważne z punktu widzenia bezpieczeństwa. Administratorzy mogą używać narzędzi do audytu, takich jak SQL Server Audit lub Oracle Database Audit, aby zobaczyć, kto miał dostęp do jakich danych i kiedy. Mogą również skonfigurować alerty, które powiadamiają ich o podejrzanej aktywności, takiej jak próby dostępu do danych poza normalnymi godzinami pracy. Wszystko to pomaga w utrzymaniu zgodności z przepisami dotyczącymi ochrony danych, takimi jak RODO.

	2.4 **Analiza trendów**: Administratorzy mogą analizować dane z monitorowania dostępu do tabel, aby zidentyfikować trendy w użyciu danych. Na przykład, mogą zauważyć, że pewne tabele są odwiedzane częściej w określonych godzinach dnia lub dniach tygodnia. Te informacje mogą pomóc w planowaniu przyszłych potrzeb zasobów i optymalizacji systemu.

	2.5 **Optymalizacja wydajności**: Na podstawie informacji uzyskanych z monitorowania dostępu do tabel, administratorzy mogą podjąć działania w celu optymalizacji wydajności systemu. Na przykład, jeśli zauważą, że pewne zapytania są wykonywane bardzo często, mogą zdecydować się na optymalizację tych zapytań, na przykład poprzez dodanie indeksów do odpowiednich tabel.

3. **Błędy dziennika i raporty**: Monitorowanie błędów dziennika i raportów jest kluczowym elementem zarządzania bazą danych. Pozwala to na szybkie wykrywanie i rozwiązywanie problemów, zanim wpłyną one na działanie systemu.

	3.1 **Dzienniki błędów**: Dzienniki błędów są zapisywane przez system zarządzania bazą danych (DBMS) i zawierają informacje o wszelkich błędach, które wystąpiły podczas działania systemu. Mogą zawierać informacje takie jak kod błędu, czas wystąpienia błędu, zapytanie, które spowodowało błąd, i inne szczegóły, które mogą pomóc w diagnozowaniu problemu. Administratorzy baz danych powinni regularnie sprawdzać dzienniki błędów i reagować na wszelkie poważne błędy. Dzienniki błędów mogą również pomóc w identyfikowaniu wzorców błędów, co może pomóc w przyszłych działaniach prewencyjnych.

	3.2 **Raporty**: Raporty są generowane przez narzędzia monitorujące i mogą zawierać informacje na temat wydajności systemu, użycia zasobów, aktywności użytkowników i innych aspektów działania bazy danych. Raporty mogą być generowane na żądanie lub automatycznie w określonych interwałach czasu. Mogą być również konfigurowane do wysyłania powiadomień e-mail lub SMS w przypadku wykrycia określonych warunków, takich jak przekroczenie progu użycia zasobów. Raporty mogą pomóc w identyfikowaniu obszarów, które wymagają uwagi, i mogą dostarczyć cennych informacji do analizy trendów i planowania przyszłości.

	3.3 **Analiza i diagnoza**: Dzienniki błędów i raporty są kluczowymi narzędziami do analizy i diagnozy problemów z bazą danych. Na przykład, jeśli system jest wolny, administrator może sprawdzić raporty wydajności, aby zobaczyć, które zapytania są najwolniejsze, a następnie sprawdzić dzienniki błędów, aby zobaczyć, czy te zapytania powodują jakiekolwiek błędy. Na podstawie tych informacji, administrator może podjąć działania w celu optymalizacji zapytań lub zwiększenia dostępnych zasobów.

	3.4 **Planowanie i optymalizacja**: Dzienniki błędów i raporty mogą również pomóc w planowaniu przyszłych potrzeb zasobów i optymalizacji systemu. Na przykład, jeśli raporty pokazują, że użycie procesora jest regularnie wysokie, administrator może zdecydować o zwiększeniu liczby rdzeni procesora dostępnych dla systemu. Podobnie, jeśli dzienniki błędów pokazują, że często występują błędy związane z brakiem pamięci, administrator może zdecydować o zwiększeniu dostępnej pamięci.

	3.5 **Zabezpieczenia i audyt**: Monitorowanie błędów dziennika i raportów jest również ważne z punktu widzenia bezpieczeństwa. Administratorzy mogą używać narzędzi do audytu, takich jak SQL Server Audit lub Oracle Database Audit, aby zobaczyć, kto miał dostęp do jakich danych i kiedy. Mogą również skonfigurować alerty, które powiadamiają ich o podejrzanej aktywności, takiej jak próby dostępu do danych poza normalnymi godzinami pracy. Wszystko to pomaga w utrzymaniu zgodności z przepisami dotyczącymi ochrony danych, takimi jak RODO.

4. **Monitorowanie na poziomie systemu operacyjnego**: Monitorowanie na poziomie systemu operacyjnego jest kluczowym elementem zarządzania bazą danych. Pozwala to na śledzenie użycia zasobów systemowych, takich jak procesor, pamięć, dysk twardy i sieć, co może pomóc w wykrywaniu i rozwiązywaniu problemów z wydajnością.

	4.1 **iostat** (*Linux*): Narzędzie iostat jest częścią pakietu sysstat w systemach Linux. Umożliwia monitorowanie statystyk wejścia/wyjścia (I/O) dla urządzeń I/O i partycji. Może pomóc w identyfikowaniu problemów z dyskiem twardym, takich jak nadmierne użycie dysku lub długie czasy oczekiwania na I/O. iostat dostarcza szczegółowych informacji na temat obciążenia dysku, takich jak prędkość transferu danych, ilość operacji wejścia/wyjścia na sekundę, średni czas oczekiwania na operację I/O i inne.

	4.2 **htop** (*Linux*): htop to zaawansowany menedżer zadań dla systemów Linux. Wyświetla listę aktualnie działających procesów i umożliwia sortowanie ich według różnych kryteriów, takich jak użycie procesora, pamięci, czasu procesora i innych. Pozwala to na szybkie zidentyfikowanie procesów, które zużywają najwięcej zasobów. htop oferuje również funkcje takie jak wyświetlanie drzewa procesów, wyszukiwanie procesów, filtrowanie procesów według użytkownika i inne.

	4.3 **vmstat** (*Linux*): vmstat to narzędzie, które dostarcza informacji o procesach, pamięci, stronach, blokach wejścia/wyjścia, aktywności procesora i dysku. Jest to przydatne narzędzie do monitorowania wydajności systemu. vmstat dostarcza szczegółowych informacji na temat użycia procesora, pamięci, dysku i sieci, co może pomóc w identyfikowaniu wąskich gardeł i optymalizacji wydajności systemu.

	4.4 **Menedżer zadań** (*Windows*): Menedżer zadań w systemie Windows umożliwia monitorowanie użycia procesora, pamięci, dysku i sieci przez poszczególne procesy i usługi. Może pomóc w identyfikowaniu aplikacji lub procesów, które zużywają nadmierną ilość zasobów. Menedżer zadań oferuje również funkcje takie jak zakończanie procesów, zmiana priorytetu procesów, monitorowanie użycia sieci i inne.

	4.5 **Monitor systemu** (*Windows*): Monitor systemu w systemie Windows jest zaawansowanym narzędziem do monitorowania wydajności systemu. Umożliwia śledzenie wielu różnych wskaźników wydajności, takich jak użycie procesora, pamięci, dysku i sieci, a także statystyki dotyczące systemu plików, bazy danych i innych komponentów systemu. Monitor systemu umożliwia tworzenie niestandardowych zestawów wskaźników wydajności, zapisywanie danych wydajności do plików logów i generowanie raportów wydajności.

5. **Monitorowanie serwera** (*np. Nagios, Grafana*): Monitorowanie serwera jest kluczowym elementem zarządzania infrastrukturą IT. Pozwala na śledzenie stanu serwerów i usług, wykrywanie problemów i analizę wydajności.

	5.1 **Nagios**: Nagios to potężne narzędzie do monitorowania systemów, sieci i infrastruktury. Pozwala na śledzenie stanu serwerów, usług sieciowych, urządzeń sieciowych i innych zasobów IT.

	Nagios oferuje funkcje takie jak:

		5.1.1 **Monitorowanie zasobów**: Nagios może monitorować zużycie procesora, pamięci, dysku, obciążenie sieci i inne metryki zasobów na serwerach i innych urządzeniach. Może dostarczyć szczegółowych informacji na temat użycia zasobów, co może pomóc w identyfikowaniu wąskich gardeł i optymalizacji wydajności systemu.

		5.1.2 **Wykrywanie problemów**: Nagios może automatycznie wykrywać problemy, takie jak awarie serwerów, przeciążenie sieci, brak miejsca na dysku i inne problemy. Może wysyłać powiadomienia e-mail, SMS lub inne, gdy wykryje problem. Może również skonfigurować alerty, które powiadamiają administratora o podejrzanej aktywności, takiej jak niezwykle wysokie zużycie zasobów.

		5.1.3 **Raporty i analizy**: Nagios generuje szczegółowe raporty o stanie infrastruktury IT, które mogą pomóc w analizie wydajności, planowaniu przyszłych potrzeb zasobów i identyfikowaniu obszarów, które wymagają uwagi. Raporty mogą zawierać informacje takie jak historia użycia zasobów, statystyki wydajności, logi błędów i inne.

	5.2 **Grafana**: Grafana to otwarte oprogramowanie do wizualizacji danych, które jest często używane do monitorowania wydajności serwerów i usług.

	Grafana oferuje funkcje takie jak:

		5.2.1 **Wizualizacja danych**: Grafana umożliwia tworzenie interaktywnych wykresów, histogramów, map ciepła i innych wizualizacji danych. Można go używać do wizualizacji metryk takich jak zużycie procesora, pamięci, obciążenie sieci, liczba użytkowników online i inne. Grafana oferuje szeroki zakres opcji personalizacji, co pozwala na tworzenie wysoce szczegółowych i informatywnych wykresów.

		5.2.2 **Integracja z różnymi źródłami danych**: Grafana może pobierać dane z wielu różnych źródeł, takich jak bazy danych SQL, systemy monitorowania jak Prometheus czy Graphite, pliki CSV i inne. Dzięki temu jest to bardzo elastyczne narzędzie, które można dostosować do różnych środowisk i potrzeb.

		5.2.3 **Alerty**: Grafana umożliwia konfigurację alertów, które mogą wysyłać powiadomienia, gdy określone warunki są spełnione. Na przykład, można skonfigurować alert, który wysyła powiadomienie, gdy zużycie procesora na serwerze przekracza określony próg. Alerty mogą być wysyłane za pośrednictwem różnych kanałów, takich jak e-mail, Slack, PagerDuty i inne.
