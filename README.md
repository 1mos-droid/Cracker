🔐 Python Hash Cracker





A fast, multiprocessing brute-force hash-cracking tool written in Python.
Supports multiple hashing algorithms, multiple character sets, real-time progress reporting, and efficient search-space generation.


---

🚀 Features

🔥 Brute-force cracking with multiprocessing

🔣 15 customizable character sets (letters, digits, punctuation, mixed variants)

🧮 Supports major hashing algorithms:

MD5, MD4, LM, NTLM

SHA-1, SHA-224, SHA-256, SHA-384, SHA-512


⏱️ Real-time progress output: iterations, hashes/sec, latest candidate

💾 Efficient memory usage: generates combinations on the fly

🔧 Automatic UTF-8 / UTF-16LE encoding based on hash type

✔️ Fully interactive CLI tool



---

📦 Requirements

Python 3.x

No external dependencies (uses only Python standard library)



---

📁 Installation

Clone the repository:

git clone https://github.com/your-username/hash-cracker.git
cd hash-cracker

Make the script executable:

chmod +x cracker.py

Run:

./cracker.py

Or:

python3 cracker.py


---

▶️ Usage

When running the tool, you'll be prompted for:

1. Character Set


2. Maximum Password Length


3. Hash Type


4. Hash Value



Example:

Specify the character set to use:

01. abcdefghijklmnopqrstuvwxyz
02. ABCDEFGHIJKLMNOPQRSTUVWXYZ
03. abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
...

Specify the maximum possible length of the password: 5

Specify the hash's type:
01. MD5
02. MD4
...

Specify the hash to be attacked: 5d41402abc4b2a76b9719d911017c592
Trying to crack hash 5d41402abc4b2a76b9719d911017c592

Example output:

Character set: abcdef..., iteration: 5120, trying: hell, hashes/sec: 1024
Match found! Password is hello

Took 3.21 seconds


---

🧠 How It Works

Generates combinations using itertools.product

Hashes each candidate string

Compares the result to the target hash

Uses multiprocessing to split workloads across character-set partitions

Reports progress at timed intervals

Stops all processes when the password is found



---

🔧 Supported Hash Algorithms

Code	Algorithm

01	MD5
02	MD4
03	LM
04	NTLM
05	SHA-1
06	SHA-224
07	SHA-256
08	SHA-384
09	SHA-512



---

🔣 Character Sets

Code	Character Set

01	a-z
02	A-Z
03	a-z + A-Z
04	0-9
05	a-z + 0-9
06	A-Z + 0-9
07	a-z + A-Z + 0-9
08	punctuation
…	up to combined alpha-num-punct


(Full list is included in the script.)


---

📊 Performance Notes

Brute-forcing is exponential and extremely intensive

Long passwords and large character sets take significantly longer

Use maximum password length and character sets wisely

CPU speed directly affects cracking performance



---

⚠️ Legal Disclaimer

This tool is intended for:

Educational use

Security research

Auditing your own passwords/systems


Do NOT use this tool for unauthorized access or malicious activity.
You are responsible for following applicable laws and regulations.


---

📜 License

Licensed under the MIT License – free to use, modify, and distribute.


---

💬 Contributing

Pull requests are welcome!
You can help improve:

Speed optimizations

New hash algorithms

Additional character-set presets

Better UI/UX printing
