Code
import random

# Pick a random number
number = random.randint(0 , 10)

guesses=0

# Now ask for guesses until the correct guess is made
done = False

while not done:
    guess = int(raw_input('Pick a number between 0 and 10(including 0 and 10)?'))
    print '					You guessed: %d' % guess
    
    if guess < number:
        print '						Higher!'
        guesses = guesses +1
    elif guess > number:
        print '						Lower!'
        guesses = guesses +1
    else:
        guesses = guesses +1
        print 'Right, you took %d tries!' %guesses
        done = True

        final = guesses
        
if guesses < 6:
        print 'Good job'
elif guesses > 5:
        print 'You are slow'
        
        done = True
