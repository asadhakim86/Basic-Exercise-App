# Basic-Exercise-App which includes a description and explanation of the separate parts of the code.
# This is the first phase code for my first project that I did by myself! I will continue to improve this by adding more input, options and functions over time!

"""Project Intro: This is a basic exercise app that allows the user to choose a number of exercises
 with varying difficulty and then the app allows you to suggest how to structure the workout
 according to the chosen difficulty. This is all done via some simple input functions"""

"""I created two functions that the app is based on by creating lists for each function which
can be indexed for any relevant input functions that I create later on in the code"""

muscle_group = ['chest', 'legs', 'shoulders', 'abs', 'arms']
difficulty_level = ['easy', 'medium', 'hard']

"""I then created a new string input function based on my muscle_group function which will allow
me to compare any input from this function to the muscle_group function during the 
relevant if and else statement."""

print('what muscle group would you like to exercise?')
muscle_group_input = str(input(muscle_group))

"""I then created a multidimensional dictionary using indexing of the initial muscle_group function.
This dictionary allows a certain muscle group within the muscle_group list to be associated with 
3 exercises based on the relevant difficulty in the difficulty_level function. Each exercise is
assigned a value from the difficulty_level function (with the help of indexing) and each muscle
group from the muscle_group list acts as the main key which is assigned the value of the
exercise and relevant difficulty level."""

Exercise = {
    muscle_group[0]: {'press ups': difficulty_level[0], 'resistance bands': difficulty_level[1],
                      'bench press': difficulty_level[2]},
    muscle_group[1]: {'body-weight squat': difficulty_level[0], 'back squat': difficulty_level[1],
                      'front squat': difficulty_level[2]},
    muscle_group[2]: {'lateral raises': difficulty_level[0], 'shoulder press': difficulty_level[1],
                      'handstand press up': difficulty_level[2]},
    muscle_group[3]: {'sit ups': difficulty_level[0], 'crunches': difficulty_level[1],
                      'front lever': difficulty_level[2]},
    muscle_group[4]: {'bicep curls': difficulty_level[0], 'tricep dips': difficulty_level[1],
                      'chin ups': difficulty_level[2]},
}

"""At this point, I created an if and else statement so that when someone inputs the muscle group they
want to workout, a number of exercises with their relevant difficulty for the chosen muscle group are 
then printed by calling and indexing the dictionary along with a string. """

if muscle_group_input == muscle_group[0]:
    print('Here are a list of chest exercises: ', Exercise[muscle_group[0]])
elif muscle_group_input == muscle_group[1]:
    print('Here are a list of leg exercises: ', Exercise[muscle_group[1]])
elif muscle_group_input == muscle_group[2]:
    print('Here are a list of shoulder exercises: ', Exercise[muscle_group[2]])
elif muscle_group_input == muscle_group[3]:
    print('Here a list of ab exercises: ', Exercise[muscle_group[3]])
elif muscle_group_input == muscle_group[4]:
    print('Here are a list of arm exercises: ', Exercise[muscle_group[4]])
else:
    print('Please input one of the muscle groups shown above!')

""" Finally, I created another if and else statement but with a new input function which 
allows the user to ask the app to suggest sets and reps for their chosen exercise based on the 
difficulty they have chosen. This was done by creating another input (sets_and_reps_input) and
another if and else statement along with it within the main if statement (a nested if/else statement)
that allows the user to index the difficulty_level function."""

print('Would you like me to suggest how many sets and reps you should aim for your exercise? State (Y/N)')
sets_and_reps = input()
if sets_and_reps == 'Y':
    print('Choose difficulty level please(0,1,2)')
    sets_and_reps_input = difficulty_level[int(input())]
    if sets_and_reps_input == difficulty_level[0]:
        print('Try 3 sets x 8 reps with 1 min breaks between sets')
    elif sets_and_reps_input == difficulty_level[1]:
        print('Try 3 sets x 12 reps with 40 sec breaks between sets')
    elif sets_and_reps_input == difficulty_level[2]:
        print('Try 4 sets x 12 reps with 30 sec breaks between sets')
elif sets_and_reps == 'N':
    print('Enjoy your workout!')
elif sets_and_reps != 'Y' or 'N':
    raise ValueError('Please state either (Y/N)!')
