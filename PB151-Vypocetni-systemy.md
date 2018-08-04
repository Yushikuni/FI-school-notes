## Laboratoř předmětu PB151 - Výpočetní systémy

**50) Assembler: přiřazovací příkaz**
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

**54) Assembler: zvýšení hodnoty proměnné o jedničku**
```assembly
udaj7c	db
	LDA udaj7c
	ADI 1
	STA udaj7c
konec0b	HLT
```

**55) Asembler: sčítání bajtových hodnot**
```assembly
suma77	db
scitd9	db
scit7d	db
B	db
C	db
	LDA scitd9
	MOV B, A
	LDA scit7d
	MOV C, A
	LDA suma77
	ADD B
	ADD C
	STA suma77
konec1c	HLT
```

**56) Asembler: inverze bitů obsahu registru**
```assembly
cislo79	db
cislo	db	255
	lda	cislo79
	mov	b, a	
	lda	cislo	
	xra	b
	mov	b, a
	mov	d, a						
konec2c	HLT
```

**57) Asembler: změna znaménka bajtové proměnné**
```assembly
cislo3f	db	
	lda	cislo3f
	cma
	inr a
 
	sta cislo3f
konec98	hlt
```
