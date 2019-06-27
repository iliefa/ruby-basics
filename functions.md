def puts_1_to_10
  (1..10).each { |i| puts i }
end

puts_1_to_10 # Ignore this for now. We'll explain it soon!

def square(n)
  puts n ** 2
end


#variable parameters

def what_up(greeting, *friends)
  friends.each { |friend| puts "#{greeting}, #{friend}!" }
end


How Blocks Differ from Methods
the block that we define will only be called once, and in the context of the array that we are iterating over.

A method can take a block as a parameter.


#combined comparison

book_1 = "A Wrinkle in Time"

book_2 = "A Brief History of Time"

print book_1 <=> book_2

prints 1

0 if equals ,1 if a>b, -1 else

##sort books in descending order

books = ["Charlie and the Chocolate Factory", "War and Peace", "Utopia", "A Brief History of Time", "A Wrinkle in Time"]

books.sort! {|a,b| b <=> a}
print books


