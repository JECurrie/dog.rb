# dog.rb
# dog.rb
class Dog
 def initialize(name)
   @name = name
   @tummy = 0 # contents of belly
end

def bark
  '%s barks' % @name
end

def exercise
  hungry? ?
 'Ignores you and looks over at his bowl.' :
 consume_energy && 'You take your dog for a walk and play with him'
end

def chase_cat
  return consume_energy && "chases #{cat.sample}" unless full? || hungry?
  "Not interested at the moment, he is #{hungry_or_full}"
end

def eat
  case @tummy
  when -30..20
  @tummy += 30
    'runs to dog bowl'
 when 21..50
 @tummy += 30
                'meanders over to the dog bowl'
              when 51..90
                @tummy += 10
                'saunters to the dog bowl'
              else
                'ignores the dog food bowl'
              end
            end
          
            private
          
            def full?
              @tummy > 90
  end
 
 def hungry?
 @tummy < 20
  end
          
            def hungry_or_full
              hungry? && 'hungry' || full? && 'full'
            end
          
def consume_energy energy = 10
 @tummy -= energy unless @tummy < 1
  end
end
          
def cat
  %w(Felix Garfield Kewtiepie)
end

my_dog = Dog.new 'Fido'
puts my_dog.chase_cat
puts my_dog.exercise
4.times do
  puts my_dog.eat
end
  puts my_dog.exercise
  puts my_dog.exercise
  puts my_dog.eat
  7.times do
  puts my_dog.chase_cat
  end
  6.times do
  puts my_dog.eat
  end  
