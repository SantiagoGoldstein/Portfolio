Przygotowanie danych: Kod wczytuje notowania indeksu S&P 500, przeprowadza ich logarytmizację oraz oblicza logarytmiczne stopy zwrotu, które są podstawą dalszego modelowania szeregów czasowych.  
HTML

Analiza statystyczna: Przeprowadzono testy normalności rozkładu (Shapiro-Wilk, Jarque-Bera), które potwierdziły, że stopy zwrotu S&P 500 nie mają rozkładu normalnego. Testy ADF i KPSS wykazały stacjonarność szeregów stóp zwrotu, a testy Mann-Kendall nie wskazały na występowanie istotnego trendu.  
HTML
+ 1

Testowanie heteroskedastyczności: Testy Ljung-Boxa oraz ARCH LM jednoznacznie potwierdziły występowanie efektu ARCH (grupowania zmienności), co stanowi naukową podstawę do wdrożenia modeli z rodziny GARCH.  
HTML

Modelowanie ARIMA: Zautomatyzowana procedura auto.arima wybrała model ARIMA(0,0,0) z niezerową średnią, co sugeruje, że logarytmiczne stopy zwrotu zachowują się jak biały szum.  
HTML

Modelowanie GARCH: Zaimplementowano model GARCH(1,1) z rozkładem t-Studenta. Wyniki wskazują na silną persystencję zmienności (suma parametrów alpha1 i beta1 bliska 1).  
HTML
+ 1

Wizualizacja: Kod zawiera zaawansowane wykresy porównujące prognozy modelu ARIMA (ceny z przedziałami ufności) oraz modelu GARCH (prognozowana zmienność) z rzeczywistymi danymi testowymi.  
HTML
