# Git: Branches

#Git #boot.dev

- Wenn du einen neuen Branch erstellst, wird der aktuelle Commit als __Branch-Basis__ genommen
- `git checkout` ist die alte Version von `git switch`

## Merge
- Merge bedeutet, dass man Zweige wieder vereint
- Dies macht man, wenn man sich sicher ist, dass die Änderungen (die man auf dem Branch gemacht hat) gut sind
- `git log --oneline --graph --all` zeigt einen Graph deiner Commits und Zweige an
- Ein __Merge-Commit__ ist der einzige Commit, der zwei Parents hat
- Mit `git log --oneline --decorate --graph --parents` kannst du nachvollziehen welcher Commit welche Eltern hat (anhand der Hashes)

### Fast-Forward-Merge
- Wenn es nur auf dem Feature-Branch (aber nicht auf dem `main`-Branch) Änderungen gibt, kommt es zu einem Fast-Forward-Merge
- Bei einem Fast-Forward-Merge entsteht _kein Merge-Commit_

## Rebase
- Rebase bedeutet die Basis eines Branch nach vorne zu verschieben
- Mit anderen Worten: Der Zweig wird an den neusten Commit rangeklebt
- Dadurch kannst du einen Fast-Forward-Merge machen
- Die Folge: Es entstehen keine Merge-Commits
- Rebase _ändert nichts_ am `main`-Branch

## Merge vs. Rebase
### Merge
- Vorteil: Erhält die korrekte Historie des Projekts
- Nachteil: Müllt die Historie mit vielen Merge-Commits zu
