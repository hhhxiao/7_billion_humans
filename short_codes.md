### 2
```
step s
pickup c
drop
```

### 3
```
step s
pickup c
step s
step s
drop

```

### 4
```
step e
pickup c
a:
step e
jump a
```

### 5
```
if e == datacube:
	a:
	step e
	jump a
endif
b:
step w
jump b
```

### 6
```
step s
step sw
step sw
step se
step e
step se
step s
step s
pickup c
```

### 7
```
a:
if s == hole:
	drop
endif
step s
pickup c
jump a
```