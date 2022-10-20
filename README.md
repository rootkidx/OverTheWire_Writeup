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
