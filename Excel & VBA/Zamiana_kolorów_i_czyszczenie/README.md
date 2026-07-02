Cel projektu: Stworzenie makra automatyzującego zmianę koloru tła oraz czcionki w zaznaczonym obszarze komórek, a także opracowanie drugiego skryptu służącego do resetowania formatowania i czyszczenia zawartości arkusza.
Folder zawiera gotowy plik xlsm z makrami
Makro do zmaiany kolorów:
```VBA
Sub ZmienKolorZaznaczenia()
    ' Sprawdzenie, czy zaznaczenie to faktycznie komórki
    If TypeName(Selection) <> "Range" Then Exit Sub
    
    With Selection
        ' Zmiana koloru tła na zielony
        .Interior.Color = vbGreen
        
        ' Zmiana koloru tekstu na czerwony
        .Font.Color = vbRed
       
    End With
End Sub
```
Makro do czyszczenia zawartości arkusza
```VBA
Sub WyczyscTloITekst()
    ' Działa na wszystkich komórkach w aktywnym arkuszu
    With Cells
        ' Usuwa kolor tła
        .Interior.ColorIndex = xlNone
        ' Przywraca domyślny (automatyczny) kolor czcionki
        .Font.ColorIndex = xlAutomatic
    End With
End Sub
```
