

## 03 - Sloppy Encryption

From my point of view as a beginner,
this was a really fun and tricky challenge :)

So you are given a string of a total of 80 individual 
characters ending with a " = " Symbol.

voilá: 
* K7sAYzGlYx0kZyXIIPrXxK22DkU4Q+rTGfUk9i9vA60C/ZcQOSWNfJLTu4RpIBy/27yK5CBW+UrBhm0=

and most importantly a sloppy.rb file which apparently holds the encryption logic implemented in
the programming language ruby !:)

<img src="solved.png" alt="PAINTU tool menu" width="60%" height="60%">

I decided to tackle this challenge by stepwise disecting the ruby code and to see what each 
ruby statement does with a given input. 

Starting with `input=gets.chomp` gets.chomp removes the line break read by gets

`h=input.unpack('C'*input.length).collect{|x|x.to_s(16)}.join`

Then the .unpack method is called which apparently seems to convert the individual
string characters into their ASCII decimal value (e.g character'a' to decimal 97)
& the individual number "collected" is converted to a string
#hexadecimal via .to_s(16) and joined to an single string via the .join method