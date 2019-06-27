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


food = false
print "we are poor" unless food


##is_true, is_false

is_true = 2 != 3

is_false = 2 == 3

##evaluate

test_1 = -11 <= 4
print test_1

## || &&

boolean_1 = (3 < 4 || false) && (false || true)

# ! to modify inplace

user_input=gets.chomp
user_input.downcase!


# ? - method to evaluate to true or false

#change string

string_to_change.gsub!(/s/, "th")

# while / until

counter = 1
until counter > 10
  puts counter
  counter += 1
end


i = 0
while i < 5
  puts i 
  i += 1
end



#for --> .. inclusive ... -> non-inclusive

for num in 1...10
  puts num
end

#iterators

##loop

i=20

loop do
  i -=1
  print" #{i} "
  break if i <= 0
end


#next

for i in 1..5
  next if i%2 == 0
  print i
end

array=[1,2,3,4,5]

array.each do |x|
  x+=10
  print " #{x} "
end


odds.each { |x| 
  x *=2
  print "#{x} "
  }

odds.each do |x|
  x *=2
  print "#{x} "
end

#times

20.times{print "x "}

#looping with for

for k in 1..50
  print k
end

#