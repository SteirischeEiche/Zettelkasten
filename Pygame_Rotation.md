# Pygame: Rotation

#Python #Pygame #programmieren

- Die Methode dreht das Objekt, indem der Rotationswinkel (`self.rotation`) verändert wird
- Delta-Time (`dt`) ist die Zeit, die seit dem letzten Frame vergangen ist
- Dh `self.rotation += ...` erhöht den Rotationswert um einen Betrag, der von der Drehgeschwindigkeit (`PLAYER_TURN_SPEED`) und der Zeit seit dem letzten Frame abhängig ist
- Dadurch bleibt die Bewegung unabhängig von der [[Pygame_Framerate|Framerate]] gleichmäßig; sie ist __zeitbasiert__, nicht __framebasiert__

## Wie funktioniert das?

```python
PLAYER_TURN_SPEED = 300  # Grad pro Sekunde

def rotate_without_dt(self):
    self.rotation += PLAYER_TURN_SPEED
```

- Wenn diese Methode bei jedem Frame aufgerufen wird, dann...
- Bei 60 FPS: `rotation` wird pro Frame um 300 Grad erhöht. Bei 60 FPS sind das 60 * 300 = 18.000 Grad pro Sekunde
- Bei 30 FPS wären es dagegen nur 9.000 Grad pro Sekunde
- Ergebnis: Je schneller der Computer, umso schneller die Drehung

### Mit `dt`

```python
PLAYER_TURN_SPEED = 300  # Grad pro Sekunde

def rotate(self, dt):
    self.rotation += PLAYER_TURN_SPEED * dt
```

- Bei 60 FPS ist Delta-Time 1/60 = 0,0167 (es müssen ja 60 Game-Loops in eine Sekunde passen)
- Dann: `self.rotation +=` 300 * 0,0167 ≈ 5 Grad pro Frame
- 60 Frames pro Sekunde * 5 Grad = 300 Grad pro Sekunde

#### Bei 30 FPS

- `dt` = 1/30 ≈ 0,0333
- 300 * 0,0333 ≈ 10 Grad pro Sekunde
- 30 Frames * 10 Grad = 300 Grad pro Sekunde (wie bei 60 FPS)
- Ergebnis: Immer die gleiche Drehgeschwindigkeit, egal wie schnell dein PC ist
