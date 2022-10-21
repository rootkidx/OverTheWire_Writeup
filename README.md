---
description: >-
  เอกสารฉบับนี้จัดทำขึ้นเพื่อเป็นการสรุปข้อมูลการศึกษา Basic Linux Command
  สำหรับตัวผู้จัดทำและอาจจะเป็นแนวทางให้กับผู้อื่นที่มีความสนใจจะศึกษา Linux
  Command
---

# OverTheWire\[Bandit] Writeup

## :triangular\_flag\_on\_post: Level 0

คือการ ssh เข้าไปยัง server **bandit.labs.overthewire.org** port **2220** โดยใช้ username bandit0 และ password bandit0

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

พอเข้ามาแล้วก็จะเป็นแบบนี้

<figure><img src="https://lh3.googleusercontent.com/Bltaxaw6LHUG5CDb14P0nSJOYZEPJYsjOP-RsCdIBtPKV9VYSFYyG7k70SRWTWZNl9vpQwKbR-soef4yKSsu5MzV5hewaJcb3d5kqkz-9QtW7-sb3DsuB5o7ZfoousN6SnaClxyn-YnSjqhJKgIeI3qcr3PrPgvu8HB7cZw6uGYxL37rH49ZGG4K9A" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 0-1

เมื่อเข้าไปยังserver แล้ว ให้ใช้ command ls -al เพื่อดูว่ามี file อะไรบ้าง

<figure><img src="https://lh6.googleusercontent.com/oaIYA8JEq7j51PagkxS0uJEF5rqhjut0fLGDbZkf54M9aJNUJZTzmxSknOUF6NQnOKBwaIXymjJcAcROBV1h7taMPIZNaugLCffgixBepYl13dLxqHP7TNrOdwNJjpCiuZfBi6iGRK_GwYC_eiGCZWOW4g27Zly1VJUjkLQCwIuXvwdLC1kqQYMjDA" alt=""><figcaption></figcaption></figure>

จะเห็นว่ามีไฟล์ readme ให้เรา cat ออกมาดู ก็จะได้ password ของข้อถัดไปนั่นเอง

<figure><img src="https://lh5.googleusercontent.com/8N8jYkP8QDWuhgREflnJ82SDratPe7zsR16AbHsh1IruN69L8Jexdc1cTxwr4ppE1mPk-b_KA2I_k1Fztj_KmOgFmX4gl4h2AbrvSMc95FxjDm65ZsziR9LPbw7PJTwMExL-lpl0Gph7d-S7H6XxI_16gIRS58wJurUNBmwLcZwkwEdcxoirYyGZmQ" alt=""><figcaption></figcaption></figure>

ให้เรานำ password ที่ได้ไป login ด้วย user bandit1

<figure><img src="https://lh5.googleusercontent.com/Is6qPKeECgXgUMCK6DR4Cm_CEZyTuzmnJKUNOxtdnGNtqb-gTXhzAFLAX_h_Wf_LpeJj0LDeqd1uWjOLNnqPMSkc5sBR3QAkgID8IgIickL7y68c1DH2kWw-U3ZT9n2Q6ZTDIN2mwl_lCZrpsJYbs6WFVee5cJ8RH9BHeriVcRzvLso87orUakl3hQ" alt=""><figcaption></figcaption></figure>

เข้าได้แล้ว เย้!!!!!

## :triangular\_flag\_on\_post: Level 1-2

> **Password : NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL**

เมื่อ ls -al จะเจอไฟล์ - (dashed file)

<figure><img src="https://lh5.googleusercontent.com/GKmF2KQ75XmzeX212uo89CbSVAGlOHps6qEx3U1F9Co7xCCZNf4rIsDKYycR64sETd2WKPUetwcLfokQPHDCzBAkux7yz8EWsbkz9EAKMKZZVNnarLoFktSuuPHvQe0cDIQ8mmAyzWF2pcy7s56FRjpngm6A9W1vEvJQHjRRXvMI7SRXSJvKdd5hHw" alt=""><figcaption></figcaption></figure>

เนื่องจากเป็น dashed file จึงไม่สามารถใช้คำสั่ง&#x20;

```
cat -
```

ให้เราใช้

```
cat < -
```

<figure><img src="https://lh5.googleusercontent.com/2CMbvMdBBhgMtH7FFTLYoLbH1j3_62e2gKASBt4AYAVPNphLiIB7kO2DGRRTCgewYBkyS149zk5pYqroN2bKmpFf_mTbTR6R10Qg231K1nVFFa-Hw9wtDXVvf0a9pfifgQrOuZvY-5paRXpatQ-viaTwLO-rkyl51Hx5gJPWOW5eSmz73Q2_mZhC5A" alt=""><figcaption></figcaption></figure>

ก็จะได้ password ออกมาแล้ว ว้าวว สุดยอดไปเลยย!!!!

## :triangular\_flag\_on\_post: Level 2-3

> **Password : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi**

เมื่อlogin ด้วยuser bandit2 และpassword จากข้อที่แล้ว ให้เรา ls ดูจะพบว่ามีไฟล์ชื่อ space in this filename ให้เรา cat ไฟล์นั้นออกมาดู แต่ๆๆๆๆๆ ถ้าเราใช้คำสั่ง **cat space in this filename** มันจะบึ้มทันที

<figure><img src="https://lh4.googleusercontent.com/Uq7nlsh-mUv3k1hUyepviIsv7ouyLXcogx4_7Q2gOGT9ooCtktr5t-bboBixV5uJzHbSWf2MU7F7u9aDkhY-mAsdyU1OJrWjncPGByt7qnqOCS5VWZhzCX7B7yhxGjAzgdqGSLx1lRua9DnZYdZgc-9d4sECOtIy5yqPwgS1-m6Y0QlVPBdrLwc0xA" alt=""><figcaption></figcaption></figure>

เพราะมันเข้าใจว่าเราต้องการจะ cat file space ,in ,this ,filename เพราะฉะนั้นอย่าหาตั้งชื่อไฟล์ที่มีการเว้นวรรคใน linux นะจ๊ะ วีธีแก้คือให้ใช้คำสั่ง

```
cat spaces\ in\ this\ filename
```

<figure><img src="https://lh6.googleusercontent.com/mCLf6l4UFl3mPa_Pt9FW2PrvaM-lxOnSpbzfPNAhLDmgZ80hi_92tufJOTQKYDrHKkCjtZVBrLDAZFRjqa6O2uKHvJuznl98fZMIdnN1rVN_d9jppF8cpd-sSAYfUaGfSWC3qCph5Wwy8xbu7D7c-FlfGspaHMUH6b1x0NY5O8rY6mQQLjIL4VLp7Q" alt=""><figcaption></figcaption></figure>

เห็นมั้ย ได้passwordแล้ววว วู้วววว

## :triangular\_flag\_on\_post: Level 3-4

> **Password : aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG**

โจทย์บอกว่า password อยู่ใน hidden file ใน inhere directory ดังนั้นให้เรา cd เข้าไปยัง inhere แล้ว ls ดูว่ามีไฟล์อะไรบ้าง

<figure><img src="https://lh5.googleusercontent.com/mS1HlS48aFWtfXN7lnFmEMeyw7oItsiL0tgztk_XyQEx5puh7qfWnWZWRGvY7zovUApWelIyDJqHpmL8MGSXwkWdq8PbSn76S-bJTmJ_8xbm_pcYcO-HJ3Hmc9Z8x2xZPdGKx9Ea0tAhSGic3MwHga0zL2MBb5ouYqEtCrvcEre5Vn2H4roBLBB8_g" alt=""><figcaption></figcaption></figure>

จะเห็นว่าไม่มีอะไรเลย เพราะมันซ่อนอยู่ยังไงล่ะ ดังนั้นให้เราใช้ ls -al มันก็จะขึ้นไฟล์ทั้งหมดออกมา แล้วให้เรา cat ออกมา ก็จะได้ password แล้วงับ

<figure><img src="https://lh4.googleusercontent.com/lEfh7zPG01BzyKFOwHEkB6ivMhhySDQWvEW7H0d2tVArTlEe5iPT5YOj1s6V3Q1B99tnG6b5bvBjMZhqW7p4pqfbp69nln6eNmGdVQVFGf8M2xkETJxQa_B8qKyTeRjdvorCzzxqPGWiLf_CVVcc4bRz4AuW9IHRitRlUMhJpeUNDJcaKDBRJCNI0Q" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 4-5

> Password : 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

เมื่อเข้ามาแล้วให้เข้าไปยัง directory inhere หลังจากนั้นให้ ls ดู จะเห็นว่ามีไฟล์เต็มไปหมด

<figure><img src="https://lh3.googleusercontent.com/Os-NZl-4io7AjwORNAv7TMLO6V7UZQ2luySA6fTzWf1t9l3_4tgK0BV5lOHUr6pJ_RbPvalserbRYbr0xC1U-HN2VBhKYD6BdpmO6T2-ZR1y3otAUd8i5nkmgE-im3-JAcK79_GfUeam6g7ZraLT5h_Vf2V9QL-NXlXwwwOjqHAXLuP_5Z2WYer1sw" alt=""><figcaption></figcaption></figure>

หลังจากนั้นลองดูว่าไฟล์ทั้งหมดคือไฟล์อะไรบ้าง

<figure><img src="https://lh3.googleusercontent.com/oqHWHyi3MadYnhQl0Ojy9uiyNUm5Jc-ihptqoedpEZ5pDDv6bYAyPlLWlMv_OymHsRAyJ5wkvMLfT88gKafZVCJuziBcSBied1SXTyOCXZ_1c0n2rtxzamN2s31wr7iJ0E2mJvaHyQY33nJu9QJDFVdv8D6T-BiTOyHmOzlNYSmFptgv84Y5YiA9Sw" alt=""><figcaption></figcaption></figure>

จะเห็นว่ามีอยู่ไฟล์เดียวที่แตกต่างจากไฟล์อื่น นั่นก็คือ **-file07** ให้เราลอง cat ออกมาดูก็จะได้passwordของข้อถัดไป

<figure><img src="https://lh3.googleusercontent.com/tc96ZxP99lMSrUKIUvUmDIkzoqR2xet9EsnMVZ-gLsqguPYGNtD3BEcZ5OEJxe2VrytYUvL4vMemwqSV3F82eMWb5xksySArdvurWKBdj9eufA-QNt2ze2D_y1SeTBKZibMed5xVIFOYj_VPAzmkiqr-ADqWIudGXJKeFfuV8kvjf_O3zPNgUULsOA" alt=""><figcaption></figcaption></figure>

## ****:triangular\_flag\_on\_post: Level 5-6

> **Password : lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR**

ข้อนี้โจทย์บอกว่า password อยู่ในไฟล์ที่มีขนาด 1033 bytes ดังนั้นเราก็ต้องใช้ข้อมูลที่ได้มาให้เป็นประโยช์โดยการค้นหาfileด้วยขนาดfile ด้วยคำสั่ง

```
find . -size 1033c 
```

<figure><img src="https://lh4.googleusercontent.com/7RkgXTF-GH77WWVrYbPMECoxyTburyk0U-l0VPtyUpNBIy3tVYl2xxEWv0V1S6WyoWIAWriX_dV71GlyLgOdz4wophk0-DXZywOawd8Y9GyQT6vhQeJz6RlsIyDQAw1JWAdF7sQoE2egl4fttb8MP_TuIWFvt_Yh2q4GqElwFVqF4zAY9F-v2JSUIg" alt=""><figcaption></figcaption></figure>

หลังจากนั้นก็ cat มันออกมา แล้วก็จะได้ password ที่ต้องการ

<figure><img src="https://lh3.googleusercontent.com/T3-WalPMHbQZFaSoBoSnk5ZiooUxT6_3iwrBzWgXjDbyO0Pqm6cpqIIpsdqpQPAp6tJ5HYotcxTp4SGTlIbZc5X8jCyZEEHYv4ZTsKYeddNnCGbon3qSt_Y_GPFRb3haufQ6Vm0oXQUI7yXGr9qBUMC8C7ATzmjBOdqrx4uoRSOkEfK0scp1MSxFWw" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 6-7

> **Password : P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU**

ข้อมูลที่ให้มา คือ owner = bandit7 , group = bandit6 , size = 33bytes ซึ่งเราสามารถ find โดยใช้ข้อมูลเหล่านี้ได้เหมือนกับข้อที่แล้วโดยใช้คำสั่ง

```
find -user bandit7 -group bandit6 -size 33c
```

จะเห็นได้ว่ามีไฟล์ขึ้นมาเยอะแยะเต็มไปหมด

<figure><img src="https://lh4.googleusercontent.com/tK3dELBuOuCnhvGeTNyjLQZn1UI4Fk3wbj4I59FiCV6A-8WFYldbPIHx_9-DfyKT12bgMg71S-Eoz1hQtnrt9tGd40pgXtR2K05PRP_m1_wCeXL2jkWrHNlKeDsGGaadIs6zHj59qYw0VAgQiMQdqamfd5VabGWI_D9QI4RFDJyl94mMjeNpZAdhTA" alt=""><figcaption></figcaption></figure>

แต่ถ้าสังเกตุดีๆจะเห็นไฟล์ที่ชื่อว่า **bandit7.password** หลังจากนั้นก็ cat ไฟล์ออกมาดูก็จะได้ password

<figure><img src="https://lh3.googleusercontent.com/XPEIE2CDasozUwIO4hJD4iuLWd1Bj1HrzlkWcraMpmivlS_pkaxWvIefukFGkxB2-Wfz7kgrGIT74_P2oTbYn2auglRSMO859FIjUjwydKnX0P-bD01lKNJDl-2lUbJ8kDQGgiFinhtlBU1MLOBTp1X2XAnRHxcdPanQVj4vgnEfGdqgIEE8rr0Yww" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 7-8

> **Password : z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S**

โจทย์บอกว่าpassword อยู่ในไฟล์ **data.txt** และถัดจากคำว่า millionth ดังนั้นเราก็ cat file data.txt แล้ว filter หาคำว่า **millionth** โดยใช้คำสั่ง

```
cat data.txt | grep millionth
```

<figure><img src="https://lh4.googleusercontent.com/qTyHFBdbcisvGK66c82jGtnIhklkxiT2B3cjbKbKtCeO3vuf7mpLJWO4IC309_bSag4ABpJVbLkEFlLdQnKSsfysZrMtzx7jeBndfcKcVdPKXKyqZgES_rDEbKa7GdV5hkZFQnno2AcL5N0a5qTbrg5Y2K-a-iqL27Ljct_EqDF2PMzt3_aCdopk7A" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 8-9

> **Password : TESKZC0XvTetK0S9xNwm25STk5iWrBvP**

Password อยู่ในไฟล์ **data.txt** ซึ่งเป็นบรรทัดที่ไม่ซ้ำกับบรรทัดอื่นเลย ให้เราใช้คำสั่ง

```
cat data.txt | sort | uniq -u
```

ซึ่งก็คือการcatเนื้อหาข้างในออกมาดูโดยทำการsortก่อน แล้วค่อยแสดงบรรทัดที่ไม่ซ้ำกับบรรทัดอื่นออกมา

สาเหตุที่ต้อง sort ก่อนก็เพราะ **uniq -u** คือการกำจัดบรรทัดที่ซ้ำกันและติดต่อกัน ดังนั้นถ้าหากมีบรรทัดที่ซ้ำกันแต่ไม่ติดกันมันก็จะแสดงออกมาด้วย

เมื่อ cat ออกมาก็จะได้ password สำหหรับข้อถัดไปแล้วจ้าาา

<figure><img src="https://lh3.googleusercontent.com/XFgCw0WxWfFSMlMnxenqjNwsqVeXUfwPwvHhIe4wlH2kFPekmn-IjC54QFD41yi3JX-c5DCWu0HBtwvVVeIlk-Ux50MesHy1ss62UBNEGuh9VT07KcvaQva_qlq8_31qIR6irY6l2veF29bVz88W8mWvEIb4hmkYtk9sB6owMfVSAJOOJn2tQ0wtjw" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 9-10

> **Password : EN632PlfYiZbn3PhVK3XOGSlNInNE00t**

Password อยู่ไฟล์ data.txt เมื่อเรา cat ออกมาดูจะเจอกับตัวอักษรอะไรไม่รู้ที่อ่านไม่ออกเต็มไปหมด ซึ่งถ้าเราเลื่อนหาดูดีๆก็จะเจอ password เพราะโจทย์บอกว่า password อยู่หลัง เครื่องหมาย = หลายๆตัว แต่ๆๆๆ มีวิธีที่ง่ายกว่านั้นคือใช้คำสั่ง

```
strings data.txt | grep =
```

<figure><img src="https://lh3.googleusercontent.com/SxqF-wBg6InSDPoMSd9gIrV0mQYsjzc5OmdauhHxp8lgmTUXI4aej1ZIxRG-19rR5TIqnLBcQtlixDAWmhI3aiRCUx0_pEufL9MmhQtmHSPBQq-zXgK1nkEGURSCMm8Q76V9qLLEunPy-8JQL2FofUj9hZDBSy4o0TB1hS_ASxu6dAGVMTx7UEhTIg" alt=""><figcaption></figcaption></figure>

เมื่อ strings ออกมาดูก็จะเห็นข้อความที่น่าจะเป็น password นั่นก็คือ **G7w8LIi6J3kTb8A7j9LgrywtEU lyyp6s**

## :triangular\_flag\_on\_post: Level 10-11

> **Password : G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s**

เมื่อ **cat data.txt** จะเจอข้อความที่ encode ด้วย **base64**

<figure><img src="https://lh6.googleusercontent.com/ghIhsJI16q0CwDZTq1D0O19zA3NIzl-0KrxDyi5cAAPYMiZkov2e5i0WAP5CrcqV8C8i0gUc0VibdR_P90HbaOtd7x5has6VTC1g8zz0eP370O4TLub6uToARvlU0AoaGiZtEMBqKDpkeYx55rbyfubChdTnHqs42jbF7CRhZEumfYxaFHfiOiJSog" alt=""><figcaption></figcaption></figure>

ให้เราทำการ decode มันออกมา ด้วยคำสั่ง &#x20;

```
cat data.txt | base64 --decode
```

<figure><img src="https://lh6.googleusercontent.com/epxsc9ZCpO9NEPBnslqs4LrFhhdx1lNSRiJgreamOCJn0RT5uTgXtcNbKAqlwlaLCcMVTuNarzfKY9mUJBnOH4ARJEH4J9eNCnWU390CGYFr_ZDldRcre3RAbM2l96wAfJP_MjoK8KZyQaV3cdzUUwN3llj-W36YuBiY9ZbWb3Esc6_NrQEHD66D-w" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 11-12

> **Password : 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM**

เมื่อเรา cat file data.txt จะเจอ strings ที่ encode ด้วยrot13&#x20;

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

ซึ่งก็คือการshiftตัวอักษรไป13ครั้ง ดั้งนั้นเราก็ต้องเลื่อนกลับมา13ครั้งเพื่อให้ได้passwordที่เราต้องการ

```
cat data.txt | tr '[a-z][A-Z]' '[n-za-m][N-ZA-M]'
```

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>



## :triangular\_flag\_on\_post: Level 12-13

> **Password : JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv**

ในข้อนี้  data.txt ที่เขาให้มาเป็นเป็นไฟล์ hexdump ซึ่งเราจะต้อง reverse มันออกมา&#x20;

```
xxd -r data.txt > data1
```

เมื่อใช้คำสั่ง file เพื่อดูว่า data1 คือไฟล์อะไร จะเห็นได้ว่ามันคือไฟล์ .gzip

<figure><img src=".gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

ให้เราทำการแปลง data1 -> data1.gz

```
mv data1 data1.gz
```

หลังจากนั้นแตกไฟล์มันออกมา

```
gunzip data1.gz
```

จะได้ data1 ที่เป็นไฟล์ .bzip

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

ให้แตกไฟล์ bzip ออกมา จะได้ไฟล์ที่เป็น gzip

```
bzip2 -d data1
```

ให้เราแปลงไฟล์ที่ได้มาจากการแตก bzip ให้เป็น .gz หลังจากนั้นให้แตกไฟล์ออกมา จะได้เป็นไฟล์ .tar

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

ให้เราแตกไฟล์ .tar ด้วยคำสั่งด้านล่างนี้ จะได้ไฟล์ที่ชื่อว่า data5.bin

```
tar -xvf data3
```

เมื่อใช้คำสั่ง file ดู file data5.bin พบว่าเป็นไฟล์ tar เหมือนกัน ดังนั้นก็ใช้คำสั่งเดิมในการแตกไฟล์มันออกมา ก็จะได้ไฟล์ data6.bin หลังจากนั้นใช้คำสั่ง file เพื่อดูว่าfile data6.bin คือ file อะไร ซึ่งคำตอบก็ไฟล์ bzip นั่นเอง&#x20;

<figure><img src=".gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

เมื่อแตกไฟล์ data6 ออกมา ก็จะได้ ไฟล์ data6 ที่เป็น .tar ให้แตกไฟล์ data6.tar ก็จะได้ data8.bin ซึ่งจริงๆมันคือfile gzip&#x20;

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

เราก็ต้องแปลงจาก .bin -> .gz

```
 mv data8.bin data8.gz
```

แล้วก็แตกไฟล์มันออกมา จะได้เป็นไฟล์ data8 ที่เป็น ASCII Text

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

ขั้นตอนสุดท้ายคือการ cat file data8 เราก็จะได้ password ที่เราต้องการแล้ว เย้ยยยยยย:tada:

<figure><img src=".gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 13-14

> **Password : wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw**

ในข้อนี้เราจะไม่ได้ password แต่เราจะต้อง get private SSH key ออกมา เพื่อนำไปเข้า user bandit14

ซึ่งเมื่อเรา SSH เข้ามาด้วย bandit13 เราจะเจอไฟล์ sshkey.private

<figure><img src=".gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

ให้เรา get มันออกมากด้วยการออกไปยังเครื่องเราก่อน แล้วใช้คำสั่ง

```
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
```

หลังจากนั้นให้เราทำการ login ด้วย bandit14 แล้วใช้ key เมื่อกี้แทน password&#x20;

```
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

จะเห็นว่ามันเข้าไม่ได้ เพราะ permission ของ key ตัวนี้มัน open เกินไป&#x20;

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

ให้เราแก้ไข permission โดยในที่นี้จะใช้เป็น 600 ด้วยคำสั่ง&#x20;

```
chmod 600 sshkey.private
```

หลังจากนั้นก็ให้ลองเข้าใหม่ จะเห็นว่าเข้าได้แล้วววววว

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

ซึ่งโจทย์บอกว่า password อยู่ใน **/etc/bandit\_pass/bandit14** ดังนั้นให้เรา cat ออกมา ก็จะได้ password แล้ว

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 14-15

> Password : fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

ในข้อนี้โจทย์บอกว่า password สำหรับข้อถัดไปอยู่ที่ port 30000 บน localhost

```
nc localhost 30000
```

เมื่อเข้าไปแล้วก็จะเจอ password สำหรับข้อถัดไปเลย

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## :triangular\_flag\_on\_post: Level 15-16

> Password : jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

password อยู่ใน localhost:30001 ให้เราเข้าผ่าน SSL&#x20;

```
openssl s_client -connect localhost:30001 -quiet
```

เมื่อเข้าแล้วก็จะเจอ password เลย

<figure><img src=".gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



