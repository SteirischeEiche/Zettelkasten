# Pygame: Endlosschleifen

#Python #Pygame #programmieren

```python
while True:
   if condition_1:
      break
```

- Dieser Code kreiert eine Endlosschleife, die unendlich lange läuft - _es sein denn_, sie wird durch `break` unterbrochen

```python
for event in pygame.event.get():
    if event.type == pygame.QUIT:
        return
```

- Dieser Code schaltet den Fenster-schließen-Knopf (rotes X) an
- Dh die Endlosschleife hört auf, wenn der User das Fenster schließt
