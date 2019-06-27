hash = {
  key1 => value1,
  key2 => value2,
  key3 => value3
}


my_hash= Hash.new

pets= Hash.new

#iterate over with each


friends = ["Milhouse", "Ralph", "Nelson", "Otto"]

family = { "Homer" => "dad",
  "Marge" => "mom",
  "Lisa" => "sister",
  "Maggie" => "sister",
  "Abe" => "grandpa",
  "Santa's Little Helper" => "dog"
}

friends.each { |x| puts "#{x}" }
family.each { |x, y| puts "#{x}: #{y}" }


languages.each{|x| puts x}

#multidimensional array 


s = [["ham", "swiss"], ["turkey", "cheddar"], ["roast beef", "gruyere"]]

s.each { |sub_array| sub_array.each { |element| puts element }}


# iterate over hash

secret_identities = {
  "The Batman" => "Bruce Wayne",
  "Superman" => "Clark Kent",
  "Wonder Woman" => "Diana Prince",
  "Freakazoid" => "Dexter Douglas"
}
  
secret_identities.each do |hero, name| 
  puts "#{hero}: #{name}"
end


# print values

matz = { "First name" => "Yukihiro",
  "Last name" => "Matsumoto",
  "Age" => 47,
  "Nationality" => "Japanese",
  "Nickname" => "Matz"
}

matz.each do |key, value|
  puts value
end


#nil

Along with false, nil is one of two non-true values in Ruby. (Every other object is regarded as “truthy,” meaning that if you were to type if 2 or if "bacon", the code in that if statement would be run.)

## false means not true, nil means nothing at all


#Symbols



menagerie = { :foxes => 2,
  :giraffe => 1,
  :weezards => 17,
  :elves => 1,
  :canaries => 4,
  :ham => 1
}
my_first_symbol= :"boss"

-used as hash keys or for referencing method names

-immutable
-one copy of any symbol exists at a given time,so they save memory
- faster than string

##convert a symbol to string

strings = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]
symbols == []

strings.each do |s| 
 symbols.push(s.to_sym)
end 
print symbols


.to_s --> convert to string
.to_sym --> convert to symbol  
.intern -->convert to symbol

new_hash = { 
  one: 1,
  two: 2,
  three: 3
}

##symbols are faster 

require 'benchmark'

string_AZ = Hash[("a".."z").to_a.zip((1..26).to_a)]
symbol_AZ = Hash[(:a..:z).to_a.zip((1..26).to_a)]

string_time = Benchmark.realtime do
  1000_000.times { string_AZ["r"] }
end

symbol_time = Benchmark.realtime do
  1000_000.times { symbol_AZ[:r] }
end

puts "String time: #{string_time} seconds."
puts "Symbol time: #{symbol_time} seconds."

###select by value 

grades = { alice: 100,
  bob: 92,
  chris: 95,
  dave: 97
}

grades.select { |name, grade| grade <  97 }
==> { :bob => 92, :chris => 95 }


movie_ratings = {
  memento: 3,
  primer: 3.5,}


movie_ratings.each_key{|k| puts k}
movie_ratings.each_key{|k| puts k}




# object id

The .object_id method gets the ID of an object

two "strings" are actually different objects, whereas the :symbol is the same object listed twice.

puts "string".object_id
puts "string".object_id

puts :symbol.object_id
puts :symbol.object_id

12928640
12928400
802268
802268

