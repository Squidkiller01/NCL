# NCL Fall 2024 Solution Notes
    Answers listed throughout are marked with quotation marks ("[answer]"). Answers should be located after the solution process.
    Different sections listed throughout a competition are underlined
    
## Individual Game

    Results: Got Gold-4 Medal and 42nd Percentile Overall
    Scoring:
        2610th PLACE OUT OF 8484
        725 POINTS OUT OF 3000
        52.6% Accuracy
        32.5% Completion

    Did not take notes
    
## Team Game

    Teammate: Wyatt Blevins
    Results: Got Platinum-3 Medal and 65th Percentile Overall
    Scoring:
        356th PLACE OUT OF 4894
        1755 POINTS OUT OF 3100
        62.3% Accuracy
        62.3% Completion
        
### __Open Source Intelligence__
    Score: 385
    Accuracy: 95.5%
    Completion: 100%
  
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
    Q2) ( Found by Teammate )
        Googling more reveals the name of the ship inside of the dome was the "Spruce Goose"
    Q3) ( Found by Teammate )
        LGB
  
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
    Score: 170
    Accuracy: 53.3%
    Completion: 72.7%

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

### Password Cracking
    Score: 60
    Accuracy: 100%
    Completion: 25%

   **Windows (Easy)**

    Using simple hash decryption tools like https://hashes.com/en/decrypt/hash will reveal the answers

    Q1) bb102cf5338be609ad2e3ef0f41d6941:081330031583
    Q2) 38dd62132565dbd1540aeaf99935e846:tiancrispatroclo
    Q3) 062133677b96285d616748ab46422e03:94022508371annie25
   
   **Combination (Medium)**

    Q1) blueflower99

### Log Analysis 
    Score: 315
    Accuracy: 51.5%
    Completion: 89.5%
    
   **Web (Easy)**

    Q1) Just count the numbers on the left side of the log. This will reveal there were "394" requests.
    Q2) ( Found by Teammate ) 
        Isolate just the file paths and error codes that are printed out and limit it to unique outputs. Use the command:
        `% cat access.log | cut -d " " -f 7,9 | sort | grep "404" | uniq -c | sort -n`
        This will reveal that "/.env" has the most 404 errors
    Q3) ( Found by Teammate )
        Print out the ip addresses, sort by only the unique occurences and then count the lines using this command:
        `% cat access.log | cut -d " " -f 1 | sort | uniq | wc - 1`
        This shows that there are "100" unique ips
    Q4) ( Found by Teammate )
        Count the numbers of times each ip occurs which shows that "212.47.65.231" has made the most requests
        `% cat access.log | cut -d " " -f 1 | sort | uniq -c | sort -n`
    Q5) ( Found by Teammate ) "46" is revealed along side the command for the previous question
    Q6) ( Found by Teammate )
        Print out every occurance of the 200 error code and then code the lines
        `% cat access.log | cut -d " " -f 9 | sort | grep "200" | wc -1`
        This reveal "175"
    Q7) ( Found by Teammate )
        Found out the largest number of bytes transferred then just searched the long for the date that transferred that much.
        `% cat access.log | cut -d " " -f 10 | sort -n`
        `% cat access.log | grep "326628"`
        This returns "Oct 30, 24"
   
   **Activity (Medium)**

    Q1) ( Found by Teammate )
        Counted the number of lines for each entry
        `% cat activity.log | sort | wc -l`
        This returned "56976"
    Q2) ( Found by Teammate )
        Isolated just the date and counted unique dates to get "173"
    Q3) ( Found by Teammate )
        Isolated just the number of events and the date to find which one had the most
        `% cat activity.log | awk -F'[":,}]+' '{print $5, $11}' | sort -k2,2n | uniq -c | sort -n`
        This reveal the answer being "2024-04-17"
    Q4) N/A
    Q5) N/A
    Q6) ( Found by Teammate )
        Search by ips and event 20 then count unique occurences
        `% jq -r '"\(.srcIp) \(.event)"' activity.log | sort | uniq -c | sort -n | grep "20" | sort -n`
        This reveals the ip being "10.238.52.234`

   **Monitor (Hard)**

    Q1) ( Found by Teammate )
        Look at the computer tag in the xml file to get the answer "DESKTOP-LIBER8"
    Q2) N/A
    Q3) ( Found by Teammate )
        Look for the event that has the process ID of 335 to get "C:\Users\User\Documents\file_6866_1730870430419.txt"
    Q4) ( Found by Teammate )
        Listed all the ports that were accessed and counted to the unique ones
        `% cat monitor.xml | grep "DestinationPort" | awk -F '[><]' '{print $3}' | sort | uniq -c`
        To get the answer "6"
    Q5) ( Found by Teammate )
        Listed the events on port 3306 and the potocol they ran on, then counted the number of times UDP appeared
        `% cat monitor.xml | grep "DestinationPort" | awk -F '[><]' '{print $3}' | sort | uniq -c`
        This revealed the answer to be "17"
    Q6) ( Found by Teammate )
        Counted the number of times the files appear to see which one appeared twice
        `% cat monitor.xml | grep "FileName" | awk -F '[><]' '{print $3}' | sort | uniq -c | sort -n`
        This reveals the file path "C:\Users\User\Documents\file_2424_1730870430418.txt"

### Network Traffic Analysis
    Score: 60
    Accuracy: 66.7%
    Completion: 44.4%
    
   **Stream'n (Easy)**

    Searching HTTP in the Display reveal the first two answeres
    Q1) 10.0.1.3
    Q2) 10.0.0.11
    Q3) Expanding the TCP section in Wireshark while having the first HTTP request selected, will reveal the port as "8000"
    Q4) Selecting the first GET request and expanding the HTTP section will reveal the user agent as "curl/8.4.0\r\n"

### Forensics
    Score: 260
    Accuracy: 62.6%
    Completion: 45.5%
    
   **Jammed (Medium)**

    Q1) Download the archive and run "unzip -FF flag1.zip" in the Linux terminal. This will repair the archive and unzip the file for the flag "SKY-CZIP-3129"
    Q2) Unlike before, we couldn't just repair the file while unzipping, we had to repair it and rezip the file using "zip -FF flag2.zip --out repaired.zip" and then unzip that file using "unzip repaired.zip" to get the flag "SKY-CZIP-1034"

### Scanning and Reconnaissance
    Score: 295
    Accuracy: 40%
    Completion: 100%
    
   **Storytime (Easy)**

    Use nmap to find and open the FTP port on the machine and ftp into the remote computer and sign in using the given credentials. Do `get -a` to copy all files from the remote machine to the local machine.
    Q1) ( Found by Teammate ) 
        Open the flags.txt files to get the flag: "SKY-GOLD-5693"
    Q2) ( Found by Teammate )
        Open the Story1.txt file to get the answer: "Labyrinth of Shadows"
    Q3) Use `ls -a` to find a hidden story file and open ".Story3.txt". This will give you the moral of the story as "Sometimes, the journey and the bond it forges are more valuable than the goal itself."

   **Vuln Recon (Medium)**

    In order to solve, just run an nmap scan on "target" by doing: `nmap -Pn -sS -T4 target`
    Q1) Port 80
    Q2) service: http
    Q3) version: Apache httpd 2.4.49
    Q4) Lookup the CVE associated with the version that we found above to find "CVE-2021-41773"

   **Feed (Hard)**

    Scan the given target to reveal that the port with the service running is port 8322.
    Q1) The scan also reveals that the port is running "TCP"
    When doing a regular scan on the port, it says the service running on the port is "garmin-marine", however this is incorrect. Run a deeper scan using this command to get question 2: `nmap -sV --version-intensity 9 -p 8322 target`
    Q2) The service running on the port is "mosquitto"
    Using the same command except adding a "-A" flag, will give us the information broadcasting from the port. The overall command is `nmap -sV -A --version-intensity 9 -p 8322 target`
    Q3) Within the information broadcasting, the flag "SKY-MQSV-8310" stands out within all the information.

### Web Application Exploitation
    Score: 0
    Accuracy: 0%
    Completion: 0%
    
    No questions solved for this section
    
### Enumeration & Exploitation
    Score: 110
    Accuracy: 60%
    Completion: 33.3%
    
   **Break-fast (Easy)**

    Q1) ( Found by Teammate )
        The programming language is "ruby"

   **Industry Guidelines (Hard)**

    Q1) The programming language is "rust"
