# Caesar_Cipher-
  ...

def CaesarCipherChar(c, k):
    a1 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ'
    a2 = 'abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz'
    if c.isalpha()==True:
        if 'A' <= c <= 'Z':
            return(a1[(a1.index(c) + k) % len(a1)])
        if 'a' <= c <= 'z':
            return(a2[(a2.index(c) + k) % len(a2)])
        else:
            return (c)
    return c 

def CaesarCipher(s,K):
    k = int(K)
    word = ''
    for c in s:
        word += CaesarCipherChar(c,k)
    return word

S = input('Enter word: ')
K = input('Enter number (1<= k <=26): ')
print(CaesarCipher(S,K))

 
