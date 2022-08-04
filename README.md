# Basic-Exercise-App
# This is the first phase code for my first project that I did by myself!

muscle_group = ['chest', 'legs', 'shoulders', 'abs', 'arms']
difficulty_level = ['easy', 'medium', 'hard']

print('what muscle group would you like to exercise?')
muscle_group_input = str(input(muscle_group))

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
