## Laboratoř předmětu PB151 - Výpočetní systémy

**50) Assembler: piřazovací řádek**
```assembly
y8b	db
xa3	db
	LDA xa3
	STA y8b
konec1d	hlt
```
**51) Assembler: vložení konstanty do registru**
```assembly
y8b	db
xa3	db
	LDA xa3
	STA y8b
konec1d	hlt
```

**52) Assembler: přesuny mezi registry**
```assembly
vzor80d	db
	LDA vzor80d
	MOV B, A
	MOV C, A
	MOV D, A
	MOV E, A
	MOV H, A
konecae	HLT
```

**53) Assembler: zvýšení hodnoty registru o jedničku (inkrementace)**
```assembly
udaja6	db
	LDA udaja6
	MOV L, A
	INR L
konec45	HLT
```
