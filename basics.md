ruby basics

integer/floats

#methods are built-in abilities of objects.

var="test phrase"
var.upcase; var.downcase,var.reverse

#comments on multiple lines
=begin
mmm
ll
=end --> multi-line comment

#input take
gets ->takes input


print "What's your first name? "
first_name = gets.chomp
print "What's your last name? "
last_name = gets.chomp


puts "name is #{first_name} #{last_name}"

user_num = Integer(gets.chomp)

#Control Flow

##if/elseif

if user_num >0
  print "positive"
elsif user_num==0
  print "0"
else
  print "negative"
end

##unless-verify something is false
hungry=false
unless hungry
  print "i'm not  hungry"
else
  print "i'm hungry"
end

##is_true, is_false

is_true = 2 != 3

is_false = 2 == 3

