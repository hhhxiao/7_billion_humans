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

### 9

```
a:
step s
pickup c
if nw == datacube:
	drop
endif
jump a
```

### 10
```
a:
if c == 1:
	step n
endif
if c == 2:
	step e
endif
if c == 3:
	step s
endif
if c == nothing or
 c == 4:
	step w
endif
jump a

```

### 11
```
pickup s
a:
step s
if w == datacube:
	drop
endif
jump a
```

### 12
```
pickup c
a:
if w != worker:
	if nw == worker:
		step s
	endif
	if sw == worker or
	 nw == wall:
		step n
	endif
	drop
endif
jump a
```

### 13
```
pickup s
a:
step e
if w == datacube and
 c != datacube:
	drop
endif
if e == wall:
	step s
	b:
	step w
	if w != wall:
		jump b
	endif
endif
jump a
```

### 14

```
pickup s
step s
step s
giveto s
```

### 15
```
a:
b:
step n
if n == datacube:
	pickup n
	c:
	step s
	if s == shredder:
		giveto s
		jump a
	endif
	jump c
endif
jump b

```
### 16
```
a:
step s
if c == datacube:
	pickup c
	b:
	step e
	if s == shredder:
		giveto s
	endif
	jump b
endif
jump a
```

### 17
```
pickup s
```




### 18
```
step sw
pickup n
a:
if s != shredder:
	step se
	jump a
endif
giveto s
```
### 19
```
a:
takefrom s
giveto se
step w
jump a
```





