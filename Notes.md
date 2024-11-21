# NCL Fall 2024 Solution Notes
## Individual Game
    
    Did not take notes
    Results: Got Gold-4 Medal and 42nd Percentile Overall

## Team Game
### Open Source Intelligence
  **Van Life (Easy)**
    
    Searching the asset models in google leads to the results.
    
    Asset A - https://www.govdeals.com/asset/222/4072
      Q1) Ford Econoline
      Q2) 2006
      Q3) Margate City
    
    Asset B - https://www.ebay.com/itm/266940624720
      Q4) Ford E-Series
      Q5) 2008
      Q6) Chicago
    
    Asset C - https://www.allsurplus.com/asset/920/5947
      Q7) Ford Econoline
      Q8) 2000
      Q9) Visalia

  **Nostalgia (Medium)**
    
    Answers can be found on https://lookup.icann.org/
    Q1) 2002-01-20 21:33:00
    Q2) Reykjavik
    Q3) ba41848820d247c1a71bcf114f7354c9.protect@withheldforprivacy.com

  **Airport (Medium)**
    
    Doing a Google reverse image search reveals the dome is the "Spruce Goose Dome" in Los Angeles.
    Q1) Going to a hash indentifier like hashes.com reveals it's a SHA-1 hash. Decrypting that hash reveals the result of "porttarget"
    Q2) Googling more reveals the name of the ship inside of the dome was the "Spruce Goose"
    Q3) LGB
  
   **Insider Threat (Hard)**
    
    Answer can be found using google reverse image search
    File 1350 leads to a woman named Lucy George
    File 2089 leads to nothing
    File 3647 leads to a guy named Jeffery Smith
    File 4821 leads to a woman named Asha Sterling
    File 7593 leads to a guy named Stuart McReynolds 
    File 9476 leads to a guy named Gary Baker
    - Therefore the answer to Q1, must be "2089".

### Cryptography

   **Bases (Easy)**
    
    Q1) Looking at this cipher, it looks to be in octal (Base-8). Decoding that reveals "3doglover9"
    Q2) This looks to be Base-16 which when decrypted, becomes "116 062 144 166 142 107 122 155 141 130 116 157 116 124 111 075", an octal cipher. When decrypted, gives the cipher "N2dvbGRmaXNoNTI=" in Base64. When decrypting, give you the answer of "7goldfish52".
    Q3) This looks to be Base64. Decoding this reveals "116 062 144 166 142 107 122 155 141 130 116 157 116 124 111 075", another octal (base-8) cipher. When decrypted again, reveals another Base64 cipher, "N2dvbGRmaXNoNTI=". Finally, decrypting this gives you the answer of "7goldfish52".
    Q4) This looks to be encrypted using binary. Decoding this reveals the octal (base-8) cipher, "115 156 112 160 144 156 154 164 131 155 106 171 111 104 143 075". Decoding this reveals another base64 cipher, "MnJpdnltYmFyIDc=". Decoding this yet again gives the shift cipher, "2rivymbar 7". Looking into the different shift ciphers, the ROT-13 cipher works to decode this into the answer "2evilzone 7".

   **Shady Shapes (Easy)**

    Watching the video, it is very easy to recognize the pattern as morse code. Dots represented by a circle and a line represented by a rectangle. Watching the whole video shows the pattern " -... / .- / -.-. / -.- / -.. / --- / --- / .-. / --- / .--. / . / -. / ..- / ... / . / -.-. / .-. / . / -.. / ... / -. / --- / .-- ".
    Q1) Translating the morse code reveals the sentence "BACKDOOR OPEN USE CREDS NOW"

   **Jefferson (Easy)**

    This can be solved by going to https://jeffersondisk.kuts.ch/. This site simulates a jefferson wheel where you can change the different configurations to match that of the assignment.
    Q1) Shifting the wheel up 8 times, reveals the answer of "Blackmailing"
    Q2) Just count the numbers in the key. In this case, there are 12 numbers in the key leading to there needing to be "12" disks.
