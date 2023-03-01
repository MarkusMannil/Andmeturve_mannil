# Praktikum 2 : Paroolide murdmine

## 1a
1) ut
2) ati
3) hack
4) hd
5) led
6) asdf

```
import string, crypt,re

# parooli räsi
encrypted = '$6$SomethingHere$L5zuxicIHC90jGVZ9xgoOjUw36DjduwH1nPGJ.uwcgLqCvhlGe6wWp55eojE9jAIXxDbcsmbAKLXuXg2AbKZo0'

# leia regexiga 

salt = re.match(r'\$.\$.*\$',encrypted)[0][0:-1]

# vaatame läbi hunniku sõnu (4 kohta) 
for c1 in string.ascii_lowercase:
    for c2 in string.ascii_lowercase:
        for c3 in string.ascii_lowercase:
            for c4 in string.ascii_lowercase:
                passwd = c1+c2+c3+c4
                if encrypted == crypt.crypt(passwd, salt):
                    print ('parool on: ' + passwd)
                    break
    
    

print('end')
```
## 2
