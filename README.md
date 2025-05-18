# sr-computer
index.html
from zipfile import ZipFile
import os

# HTML কোড
html_code = '''<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SR Computer Training Centre</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      line-height: 1.6;
    }
    /* অন্যান্য CSS এখানে আছে */
  </style>
</head>
<body>
  <!-- পুরো HTML বডি এখানে পেস্ট করুন (আগের দেওয়া মোবাইল ফ্রেন্ডলি ভার্সন) -->
</body>
</html>'''

# HTML ফাইল সেভ করুন
with open("index.html", "w", encoding="utf-8") as file:
    file.write(html_code)

# ZIP ফাইল তৈরি করুন
with ZipFile("sr_computer_site.zip", "w") as zipf:
    zipf.write("index.html")

# প্রয়োজন না হলে index.html মুছে ফেলুন
os.remove("index.html")

print("ZIP ফাইল তৈরি হয়েছে: sr_computer_site.zip")
