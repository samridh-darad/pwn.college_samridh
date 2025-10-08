## A Memory's a Heavy Burden
You now find yourself in the place where many climbers have been laid to rest. A cold wind moves through the temple grounds, carrying whispers of the departed. Stone lanterns and marble graves reflect Buddhist traditions, their shadows stretching across the frost-covered earth.

The temple rests in the shadow of a very iconic mountain, quiet and imposing. Every detail in the image, the arrangement of the graves, the lanterns, and the lingering scent of incense, holds clues to its true location. You need to uncover the exact coordinates of where you are to move on from here.

Note: round off coordinates to 3 decimal places.

Flag format: citadel{XX.XXX_XXX.XXX}

### Solve
**Flag:** `citadel{35.486_138.699}`

1. Searched the place using google lens.
2. Found a reddit post in which it's location was mentioned 
3. Used that location to get the coordinates of the place and got the flag.
https://www.reddit.com/r/geoguessr/comments/1nygdv7/can_someone_help_me_find_this_exact_place/?tl=hi


### New Learnings
Leaarned to locate coordinates using different sources on the internet using different platforms.

### References 
No refrences used.




## BRATCHA
A clear chime rolls through the chamber and a new crest ignites on your badge – a quiet promotion. The outer ring is behind you. From here, the Citadel opens its inner systems, and the locks grow heavier because the keys are worth more. Your answers now carry more weight – and earn more in return. The citadel welcomes you to the inner climb.

Near the gate to the next floor you come across a CAPTCHA verification test, but it has been covered by scratches on the decaying wall and misleading letters stopping you from finding the correct key, all to prove you’re human.

### Solve
**Flag:** `citadel{1m_3v3rywh3r3_1m_s0_jul1a}`

Every letter of the url had the possibilities of two letters so, used the python code with the help of AI to try every possibilities i.e 2^8 possibilities of the link were tried using the code on the website and found the correct url.

```py
import requests
from itertools import product

BASE_URL = "https://pastebin.com/"

# Possible characters for each position
options = {
    1: ['c', 's'],
    2: ['g', 'q'],
    3: ['x', 'y'],
    4: ['h', 'n'],
    5: ['v', 'w'],
    6: ['b', 'd'],
    7: ['m', 'n'],
    8: ['s', 'z']
}

# Generate all possible links
def generate_links(char_choices):
    for guess in product(*(char_choices[pos] for pos in sorted(char_choices))):
        yield BASE_URL + "".join(guess)

def find_valid_link():
    for url in generate_links(options):
        try:
            resp = requests.get(url, timeout=5)
            if resp.ok and "pastebin.com" in resp.text:
                print(f"[✔] Found link: {url}")
                return url
            else:
                print(f"[x] Invalid attempt: {url}")
        except requests.RequestException:
            continue
    return None

if __name__ == "__main__":
    link = find_valid_link()
    if not link:
        print("No valid link found.")

```

### New Learnings
Learned about brute forcing.

### References 
Used ChatGPT.



## The Ripper
The guardian of this floor steps from the shadows. Known only as Jack the Ripper, he watches you carefully. He proclaims himself merciful and hands you a word list to help. He asks you to find the passcode hidden in this hash $2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa. The word list is your only aid. Only by combining the two correctly can you uncover the key and move on to the next floor. Flag format: citadel{password}

### Solve
**Flag:** `citadel{fake_flag_4_fake_pl4y3rs}`

This is decryption problem so, used added john module in linux terminal and got code with the help of AI to use john module to decrypt the passcode as I had familiarity with john command because it was also used in PWN college challenge.

```bash
echo '$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa' > hash.txt && \
john --wordlist=wordlist.txt --format=bcrypt hash.txt && \
john --show hash.txt
```

### New Learnings
Learned to use john module in linux terminal for decryption.

### References 
Used ChatGPT.




## Test of Sweetness
This floor feels like a digital world. The space is an illusion, all pink and sweet, stretching around you in impossible patterns. Here, you are no longer a climber but just another user.

Ahead, a door glows faintly. It is the only path forward and requires a level of authority you do not yet have. Fragments of session memory flicker, hinting at what it might take to gain higher access.

### Solve
**Flag:** `citadel{fru1tc4k3_4nd_c00k13s}`

Went to website opened it's dev tools by f12 and in cookies changed user to admin and got the flag.
![alt text](image.png)

### Learned about 
Learned to use cookies which store memories to changed the authority access of the website and get control.

### References 
Disccused with team.




## The Sound of Music
🗼OSINT pt2: citadweller had a newfound interest in tracking the music they last listened to and posting ratings of new albums on various online platforms.

The flag is hidden in these digital footprints across music platforms and split into three segments. You will need to find all three to uncover the complete code and move on to the next floor.

### Solve
**Flag:** `citadel{c0mputers_st0pped_exchang1ng_1nf0rmat10n_n_started_shar1ng_st0r1es_n_then_they_were_n0where_t0_be_f0und}`

Tried to find citadweller album on last.fm since last was emphasized at first but after a lot of time found citadweller account on last.fm which had one part of the flag. After that found second part in rate your music, also it had the link of spotify which gave the third part of the flag thus completing the whole flag.

### New Learnings
Learned to collect data from different platform across internet.

### References 
No references used.

