Model Lee-Cartera. Przedstawione dane mają charakter poglądowy i służą do demonstracji działania autorskiej funkcji zaimplementowanej w języku VBA.
Funkcja:
```VBA
Function LeeCarter(ax As Double, bx As Double, kt As Double) As Double
    ' Oblicza współczynnik śmiertelności m(x,t) wg modelu Lee-Cartera
    ' Formuła: m_xt = exp(a_x + b_x * k_t)
    
    LeeCarter = Exp(ax + bx * kt)
End Function
```
  


