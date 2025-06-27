# Pygame: Framerate

#Python #Pygame #programmieren

- Wenn man keine Framerate festlegt, zeichnet der Computer den Bildschirm sooft wie möglich neu
- Das verbraucht unnötig viele CPU-Ressourcen

## Delta-Time

- Delta wird in der Mathematik verwendet, um die Änderung eines Wertes darzustellen
- In der Spieleentwicklung verwendet man Delta-Time, um die Zeit darzustellen, die seit dem letzten Bild (Frame) vergangen ist
- Damit kann man das Spiel von der Bildschirmaktualisierungsrate entkoppeln
- Dh Spiel behält die gleiche Geschwindigkeit bei, egal wie schnell oder langsam der Computer ist
- (Wird der Computer langsamer, wird das Spiel nur weniger flüssig aber nicht langsamer)

## FPS festlegen

- Zunächst erstellt man ein Clock-Objekt und eine Delta-Time-Variable

```python
clock = pygame.time.Clock()
dt = 0
```

- Am Ende jeder Spielschleife (game loop) rufen wir die `.tick()`-Methode auf: `clock.tick(60)`
- `.tick()` sorgt hier dafür, dass die Schleife solange pausiert, bis 1/60 einer Sekunde vergangen ist
- __Dh das Spiel wird auf 60 FPS limitiert__
- Außerdem gibt `.tick()` Delta-Time zurück
