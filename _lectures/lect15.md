---
num: "lect15"
lecture_date: 2019-05-30
desc: "Character Encoding"
ready: true
pdfurl: /lectures/pdf/lect15.pdf
annotatedready: false
---

<a href="{{page.pdfurl | relative_url }}" data-ajax="false">Slides PDF</a>

# Python Demo Code Used

Try these out again on IDLE and re-live the glory times from class... :)

```py
def myCipher(myStr):
    newStr = ""
    for c in myStr:
        i = chr(ord(c) + 1)
        newStr += i
    return newStr

print(myCipher("come to the zoo at noon or the penguin gets it!!!"))


def deCipher(myStr):
    newStr = ""
    for c in myStr:
        i = chr(ord(c) - 1)
        newStr += i
    return newStr

print(deCipher("ifmmp"))
print(deCipher('dpnf!up!uif!{pp!bu!oppo!ps!uif!qfohvjo!hfut!ju"""'))
      
print(deCipher(myCipher("I am a spy!")))


def MirrorEncrypt(message): # message is a string type
    result = ''         # start with an empty result
    for c in message:   # go thru every letter in message
                        # let’s apply the “mirror” formula:
        nc = ord(c)
        nr = ord('a') + ord('z') - nc

		# then accumulate the encoded chars, one at a time
        result = result + chr(nr)
    return result

print(MirrorEncrypt("abcdefghijklmnopqrstuvwxyz"))

print(MirrorEncrypt("meet me at the zoo or the giraffe is next!"))

print(MirrorEncrypt("nvvg»nv»zg»gsv»all»li»gsv»trizuuv»rh»mvcgº"))

print(MirrorEncrypt(MirrorEncrypt("I love CS8")))

print(MirrorEncrypt("CAT"))
print(MirrorEncrypt("Cat"))

```
