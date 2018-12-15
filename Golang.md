# GO
Golang ist eine Sprache von Google, die in eine ausführbare Datei compiled wird, sodass es schnell und resourceneffizient ist.
## Schleifen
In Golang gibt es nur eine `for` Schleife, mit der aber sehr viel machen kann.
### While true
```golang 
for {
    ....
}
```
### While Schleife
```golang 
for Condition{
    ....
}
```
### Do While Schleife
```golang 
for {
    ....
    if Condition {
        break
    }
}
```
### For
```golang 
for i:=0; i<10; i++{
    ....
}
```
### Array durchlaufen
Um eine Array zu durchlaufen, gibt es mehrere Möglichkeiten.
```golang 
for index, element := range array {
    ....
}
```
In der Schleife kann man immer auf das Element zugreifen, ausßerdem bekommt man den Index im Array

