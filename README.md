# verbose_login
Yeh code ek Python script hai jo email enumeration ke liye use hoti hai. Yeh script TryHackMe (THM) ke verbose_login module par test karne ke liye banayi gayi hai.

Code Explanation (Hinglish)
check_email(email):

Yeh function email check karta hai aur request send karta hai login API par.
Response JSON format mein return hota hai.
enumerate_emails(email_file):

Email list ko file se read karta hai.
Har email par check_email() function run karta hai.
Agar "Email does not exist" message aata hai toh woh invalid hai.
Warna email valid hai aur usko list mein add kar diya jata hai.
if __name__ == "__main__":

Command-line argument se email list file leta hai.
enumerate_emails(email_file) call karta hai aur valid emails print karta hai.

How to Use 
Save this code as script.py.
Run the script terminal me:
  # python3 script.py emails.txt
(yahan emails.txt ek file hai jo email list contain karti hai.)
# Output milega:
          [INVALID] test@example.com
          [VALID] admin@target.com
Yeh script user enumeration vulnerability check karne ke liye useful hai.
