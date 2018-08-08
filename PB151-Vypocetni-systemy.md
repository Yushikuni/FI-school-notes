## Laboratoř předmětu PB151 - Výpočetní systémy

**50) Asembler: přiřazovací příkaz**
```assembly
y8b	db
xa3	db
	LDA xa3
	STA y8b
konec1d	hlt
```
**51) Asembler: vložení konstanty do registru**
```assembly
y8b	db
xa3	db
	LDA xa3
	STA y8b
konec1d	hlt
```

**52) Asembler: přesuny mezi registry**
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

**53) Asembler: zvýšení hodnoty registru o jedničku (inkrementace)**
```assembly
udaja6	db
	LDA udaja6
	MOV L, A
	INR L
konec45	HLT
```

**54) Asembler: zvýšení hodnoty proměnné o jedničku**
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
**58) Asembler: nastavování příznaků SF a ZF**
```assembly
cislo70	db
	LDA cislo70
	ADI 0
konec8c	HLT
```

**59) Asembler: nastavení příznaku CF a vynulování AF**
```assembly
cislo88	db	0e6h
cislo	db	e0h
	lda cislo
	mov b, a
	lda cislo88
	add b
konec80	hlt
```

**60) Asembler: vynulování příznaku CF a nastavení AF**
```assembly
cislo80    db 0b2h
    lda cislo80
    adi 15
konec09    hlt
```

**61) Asembler: nastavení příznaku parity**
```assembly
argh	db	3
abcd	db	12
	lda	argh
	mov	b, a		
	lda	abcd
	add	b

konec9a	hlt
```

**62) Asembler: testování shody**
```assembly
x07a	db
ydf0	db
	lda	x07a
	mov	b, a
	lda	ydf0
	cmp	b
	jnz	shoda
	inr	e
shoda   add	e

konec86	HLT
```

**63) Asembler: testování neshody**
```assembly
x4da	db
y1d1	db
	lda	x4da
	mov	c, a
	lda	y1d1
	cmp	c
	jz	shoda
	inr	d
shoda   add	d

konecff	HLT
```

**64) Asembler: testování shody**
```assembly
x07a	db
ydf0	db
	lda	x07a
	mov	b, a
	lda	ydf0
	cmp	b
	jnz	shoda
	inr	e
shoda   add	e

konec86	HLT
```

**65) Asembler: detekce přeplnění při sčítání celých čísel bez znaménka**
```assembly
x312	db
y49d	db	
	lda	x312
	mov	b, a
	lda	y49d
	add	b
	jnc 	konecce
ovrflw4	HLT
konecce	HLT
```

**66) Asembler: detekce přeplnění při odčítání celých čísel bez znaménka**
```assembly
x978	db
yfdd	db
	lda	yfdd
	mov	b, a
	lda	x978
	sub	b
	jnc	koneccb

ovrflwc	HLT
koneccb	HLT
```

**67) Asembler: testování menší nebo rovno (znaménkem výsledku)**
```assembly
xd92	db	
y54a	db
	lda	xd92
	mov	c, a
	lda	y54a
	cmp	c
	jm	koneccc
bud	mov	a, l
	cma
	mov	l, a
	
koneccc	HLT
```

**68) Asembler: testování ostře větší než (znaménkem výsledku)**
```assembly
xe96	db
y2c4	db
	lda	xe96
	mov	b, a
	lda	y2c4
	cmp	b
	jp	konecfe
anebo:	mov	a, l
	cma
	inr	a
	mov	l, a
	
konecfe	HLT
```

**69) Asembler: testování větší nebo rovno (znaménkem výsledku)**
```assembly
xe88	db	
yd54	db	
zvys	db	69		
	lda	zvys	
	mov	d, a
	lda	yd54
	mov	b, a
	lda	xe88
	cmp	b
	jm	konecf3
anebo:	mov 	a, e
	ADI	156
	mov	e, a
konecf3	HLT
```

**70) Asembler: detekce přeplnění při sčítání celých čísel se znaménkem**
```assembly
	adv	of	
xc52	db
y10d	db
	lda	xc52
	mov	b, a
	lda	y10d
	add	b
	jo	ovrflw9
nebud	lda	xc52
	cma	a
	inr	a
	sta	xc52
	jmp	konec98
ovrflw9	HLT
konec98	HLT
```

**71) Asembler: porovnání velikosti čísel bez znaménka**
```assembly
	adv of
xd50	db
yebc	db
	lda	xd50
	mov	b, a
	lda	yebc
	cmp	b
	jae	ano54
ne54	HLT
ano54	HLT
```


**72) Asembler: porovnání velikosti čísel se znaménkem**
```assembly
	adv of
x2e3	db
ydee	db
ano	db	1
ne	db	2
	lda	ydee
	mov	b, a
	lda 	x2e3
	cmp	b
	JLE	bud
nebud	lda	ne
	mov	e, a
	jmp	ne62
bud	lda	ano
	mov	e, a
	jmp	ano62

ano62	HLT
ne62	HLT
```

**73) Asembler: použití registrů H, L a M**
```assembly
	LXI	H, 46944
	MOV	M, E
	LXI	H, 5465
	MOV	A, M

konec15	HLT
```

**74) Asembler: sčítání 16bitových čísel**
```assembly
xlow64	db
xhigh64	db
ylow64	db
yhigh64	db
zlow64	db
zhigh64	db
	lda	xlow64
	mov	b, a
	lda	xhigh64
	mov	c, a
	lda	ylow64
	mov	d, a
	lda	yhigh64
	mov	e, a
	lda	zlow64
	mov	h, a
	lda	zhigh64
	mov	l, a
	lda	xlow64
	add	d
	sta	zlow64
	lda	xhigh64
	adc	e
	sta	zhigh64
konec86	HLT
```

**75) Asembler: Asembler: operace prováděné v cyklu**
```assembly
kolik4e	db
zacatek	lda kolik4e
	cpi 0
	jz konecee
	dcr a
	sta kolik4e
pridani	mvi m , 30
	mov a , l
	adi 1
	mov l , a
	mov a , h
	aci 0
	mov h , a
	jmp zacatek	
konecee	hlt
```

**76) Asembler: záměna obsahů registrů pomocí zásobníku**
```assembly
	lxi sp, 63554
	push d
	push b
	pop d
	pop b
konec60	hlt
```

**77) Asembler: použití volání podprogramu**
```assembly
wc11	db	
x103	db
ybb3	db
zf1c	db
	lda	wc11
	mov	b, a
	lda	x103
	call	odectia
	lda	ybb3
	call	odectia
	lda	zf1c
	call	odectia
konec6b	HLT
odectia:	CMA
	inr	a
	add	b
	mov	b, a
	RET
```
