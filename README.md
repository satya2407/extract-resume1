# extract-resume1
import re
f = open("C:\\Users\\SAI\\Downloads\\fullresume.txt","r")
line1 = f.read()    
match = re.findall(r'[\w\.-]+@[\w\.-]+', line1)
num = re.findall('\+?\d[\d ]{8,12}\d',line1)
date1 = re.findall('(\d+/\d+/\d+)',line1)
date2 = re.findall('(\d+-\d+-\d+)',line1)
phone2 = re.findall('[0-9\ \(\)\+]{6}',line1)
name =  re.findall('([a-zA-Z]{3,30}\s*)+[a-zA-Z]{3,30}',line1)
address = re.findall('^\d+\s[A-z]+\s[A-z]+',line1)
###name2 = re.findall('(^$)|(^([^\-!#\$%&\(\)\*,\./:;\?@\[\\\]_\{\|\}¨ˇ“”€\+<=>§°\d\s¤®™©]|)',line1)
print("Pincode")
print(phone2[0])
print("Email id")
for i in match:
    print(i)   
print("Date of birth")
for i in date1:
    print(i)
for i in date2:
    print(i)
print("Phone number")
print(num[0])
print("Name")
print(name[0])
