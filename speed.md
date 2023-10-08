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

### 13
```
step s
pickup c
if w == nothing:
	step w
	a:
	step se
	if se == wall:
		step ne
		step n
		step n
		drop
		b:
		jump c
	endif
	jump a
endif
if e == nothing:
	step se
	step se
	drop
	jump b
endif
step s
step s
d:
e:
step e
if e == wall:
	step s
	step s
	f:
	step w
	if c == nothing:
		drop
		jump g
	endif
	if w == wall:
		step s
		step s
		jump d
	endif
	jump f
endif
jump e
g:
c:
step n
```

### 14
```
if s == datacube:
	pickup s
	step s
	step s
	giveto s
endif
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
step s
step s
step se
if nw == nothing and
 se == worker:
	step s
	step s
	pickup sw
	step e
	step e
	step e
	step se
	step e
	giveto s
endif
if nw == worker and
 se == nothing:
	pickup sw
	step e
	step e
	step se
	giveto s
	step s
	end
endif
a:
if w == nothing and
 e == nothing:
	step s
	pickup sw
	step e
	step e
	step e
	step se
	giveto s
	step n
	end
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




