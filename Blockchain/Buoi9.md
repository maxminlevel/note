ma hoa trong blockchain
thầy Thuc 

Cac cong nghe trong Blockchain
- Game theory
- P2P
- Cryptography:
  + Publickey cryptosystem (ECC)
  + Cryptographic hash function (SHA)

Crypto System

```
E_k
```

PP Encry
- Permuatation
- Subtutiation

Tieu chi cua thuat toan ma hoa
- Security: Khong gian M, C, K du lon (chong vet can)
- Key-Exchange: on secure channel

VD: 
    Doc === BLOCKCHAIN (Plain doc)
    |
    | Encode
    |
    01111302... (Plaintext)
    | Encrypt
    | 0123456789=4721589630
    |
    47777142... (Ciphertext
    
Cac he ma: D_k'(E_k(m))m
TH1: k === k': Ma doi xung/ ma khoa bi mat
TH2: k !=== k': Ma bat doi xung/ khoa cong khai
  k: khoa ma hoa, e = k
  k': khoa giai ma, d = k'
TH3: 
2 trh dau la ma hoa, trh nay E chi can 1 chieu (giau thong tin) One way function (Ham bam mat ma)


Public key cryptosystem:
PP: D/n 1 ham hona vi tren Z_n la ham 1 chieu co trapdoor (Oneway funct method)
Dung 1 bai toans kho (Hard problem cho may tinh)
- Phan tich thua so nguyen to: IFP (Intergr factorization problem)
    + Cho n = pq (1024bit) tim p 
    + ung dung trong RSA
    + Pho bien hon nhng so bit dai
- Bai toan log roi rac DLP (Discrete Logarthm problrm)
    + Cho g, y = g^x % p, p tim x
    + Ung dung trong diffie-hellman

Tap vong: Z_n={0,1,2,...,n-1} voi (x,y) = (x*y) % n
1. Z_n ko ton tai x ===_n y trong Z/n <=> y = x%n
2. x thuoc Z_n kha nghic (mod n) <=> Ton tai y thuoc Z_n sao cho (x*y) %n = 1
3. Zn+ la tap kha nghich. Zn+ = {x} sao cho x kha nghich mod n
3a. x^-1(mod n) = y^-1(mod n) <=> x*y mod n = 1
3b. GCD(x,n) = 1

RSA Protocl
m thuoc Alice public (e, n)             Bob (e,d)
1. p,q = primeGen(x) // tao 2 so nguyen to lon p, q
2. n = pq, phi = (p-1)(q-1)
3. Chon e,d: ed % phi = 1 (e, d thuoc Zphi+)
    Cong bo n, e: Giu bi mat p,q,phi,d
4. c = m^e%n
5. m = c^phi%n

VD: p = 5, q = 7
n = 35, e = 24
e = 5, d = 5
m = 2 -> c = 2^5 % 35 = 32
         m = 32^5 % 35 = 2

PP tim e,d : CHon e le, bieu dien ex + phi y = gcd(e,phi). 
  Neu khac 1 thif chon e = e+2
  Neu = 1 thi ex % phi = 1 -> d = x
Thuat toan: XEuclid, Bezout

BT: Cho p,1 sinh e,d va ma m = 2; m = 3