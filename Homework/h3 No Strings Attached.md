# a)
To get the .zip in my vm i use curl (wget work too) and unzip it with unzip
![screenshot](screenshot/H3/{DE4CC2CA-72C2-4A5A-923A-1A0CBD192E42}.png)
![screenshot](screenshot/H3/{4416CAB0-74CE-4975-88C1-31EA3EAB8600}.png)
![screenshot](screenshot/H3/{A04189C6-15B6-4389-846E-84EF5A1C4EAA}.png)
we use string to see whats going on in the executable
![screenshot](screenshot/H3/{81C42ABF-14C1-4869-9223-82C564893A37}.png)

we can see the password  and the flag by looking at it
![screenshot](screenshot/H3/{93DA2B7C-1FBE-4CA9-90E0-F1059388B617}.png)
i have just verified that it is the password and it is
![screenshot](screenshot/H3/{875CB415-4D6C-4DED-BDFE-67367937223B}.png)
and so the flag is : FLAG{Tero-d75ee66af0a68663f15539ec0f46e3b1}
# b)

for obfuscate the password i just decompose the string in many little string 

![screenshot](screenshot/H3/{825C87EC-D17C-41A2-807F-AB3696FCB990}.png)


before :
![screenshot](screenshot/H3/{4360D2DD-AE91-4FDB-A862-7FA11EC61FED}.png)

after : 
![screenshot](screenshot/H3/{F99BF6BB-3F8A-4DCE-A96B-D84F90F9E638}.png)
we can see that the password isn't visible now

# c)

now for the Packd we can see when we strings the file we see UPX so i just try to use upx in the terminal and i saw  that it was a command

![screenshot](screenshot/H3/{D82C9128-3AED-4A06-BEC9-8ABE42E38510}.png)

to see how it work i look at the the -h  and we see that -d decompress 


![screenshot](screenshot/H3/{CD0E32EC-8803-491F-8371-EB3A50B70791}.png)

we can now  upx -d packd


![screenshot](screenshot/H3/{13BAB210-FA8B-4D1E-A726-9127B54DA4F5}.png)

and now we can strings the file 
![screenshot](screenshot/H3/{7C6BFC17-EA40-4957-BA0D-2BD82F1BE1F9}.png)
now we have the password and the flag
![screenshot](screenshot/H3/{CA05582E-F954-436A-8905-AE5E44DA3B6A}.png)
password : piilos-AnAnAs 
and the flag is FLAG{Tero-0e3bed0a89d8851da933c64fefad4ff2}