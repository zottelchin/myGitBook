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
### Unendlich lange Warten
Tut einfach nichts, braucht aber lange. Select wartet eigentlich auf die Rückgabe eines Chanels, wenn es keinen gibt, wartet es halt sehr lange.
```golang
select {}
```
In der Schleife kann man immer auf das Element zugreifen, ausßerdem bekommt man den Index im Array

## Type Assertion
### Type Switch
```golang
switch val := c.Value.(type) {
	case string:
		return val
	case int:
		return strconv.Itoa(val)
	case int16:
		return strconv.FormatInt(int64(val), 10)
	case int32:
		return strconv.FormatInt(int64(val), 10)
	case int8:
		return strconv.FormatInt(int64(val), 10)
	case int64:
		return strconv.FormatInt(val, 10)
	case float32:
		return strconv.FormatFloat(float64(val), 'f', 3, 32)
	case float64:
		return strconv.FormatFloat(val, 'f', 3, 64)
	case bool:
		return strconv.FormatBool(val)
	}
	return ""
```
### Type Assertion
```golang
t := i.(T)
...
t, ok := i.(T)
...
```
## Crosscompiling
Für Standart Go reicht: `GOOS=linux go build`
Wenn SQLite verwendet wird, wird es etwas aufwendiger. Dann braucht man `CGO_ENABLED=1 GOOS=linux go build`
