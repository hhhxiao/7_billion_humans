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
step s
if c == datacube:
	pickup c
	b:
	step s
	if s == hole:
		drop
	endif
	jump b
endif
jump a

```

### 9
```
pickup s
a:
step s
if w == datacube:
	step s
	drop
else:
	jump a
endif
```

### 10
```
a:
if n != hole:
	step n
else:
	jump b
endif
jump a
b:
c:
if w != hole:
	step w
	jump c
else:
	jump d
endif
d:
step sw
step sw
step s
step sw
step w
step w
step w
step nw
step n
step n
step n
step n
step nw
```

### 11
```
-- 7 Billion Humans (2235) --
-- 11: 注入数据 1 --
pickup s
step s
step s
step s
step s
a:
if w == datacube and
 c == nothing:
	drop
	b:
	step s
	jump b
else:
	step s
	step s
	jump a
endif
```

### 12
```
pickup c
if w == wall:
	step n
	drop
else:
	if e == wall:
		step s
		drop
	else:
		a:
		if nw == worker:
			step s
			jump b
		endif
		if sw == worker:
			step n
			jump c
		endif
		if se == worker:
			step n
			jump d
		endif
		if ne == worker:
			step s
			jump e
		endif
		jump a
	endif
endif
b:
c:
d:
e:
drop
```