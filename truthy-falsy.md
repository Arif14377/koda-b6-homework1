# Nilai Truthy dan Falsey
## Nilai Truthy
- Nilai truthy adalah nilai yang dianggap true ketika ditemui dalam konteks boolean.
- Semua nilai adalah truthy kecuali jika didefinisikan sebagai falsy.

contoh nilai truthy dalam javascript (yang akan diubah menjadi nilai true dalam konteks boolean, dan akan mengeksekusi blok if) :

if(true);
if({});
if([]);
if(42);
if(0);
if("false");
if(new Date());
if(-42);
if(12n);
if(3.14);
if(-3.14);
if(Infinity);
if(-Infinity);

### Operand &&
jika operand pertama adalah truthy, maka perbandingan operator akan mengembalikan operand kedua:
true && "dog"; //returns "dog"
[] && "dog"; //returns "dog"

## Nilai Falsy
Nilai Falsy (terkadang ditulis Falsey) adalah nilai yang dianggap false ketika ditemui dalam konteks boolean.

berikut adalah list nilai falsey javascript:
null                : Tidak ada value apapun
undefined           : primitive value
false               : boolean (keyword false)
NaN                 : Not a Number
0                   : Number zero. termasuk 0.0, 0x0, dll.
-0                  : Negatif zero, termasuk -0.0, 0x0, dll.
0n                  : BigInt zero, termasuk 0x0n.
""                  : string kosong, termasuk '', ``

### Operand &&
jika operand pertama adalah falsey, maka perbandingan operator akan mengembalikan operand pertama:
false && "dog"; //returns false
0 && "dog"; //returns 0