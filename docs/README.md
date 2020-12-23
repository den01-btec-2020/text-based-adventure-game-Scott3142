# Documentation for the text-based adventure game

The documentation is written using Google Workspace, so live links to each documentation file can be found below:

- [Design document](https://docs.google.com/drawings/d/1hk0iuTjYdJrHFCGE-1ty4Fp9m_jciWms-G6Eb7T-XPo/)
- [Algorithm](https://docs.google.com/drawings/d/1I-VNnaS5L6YW5OHL6g_uexH5jIdVyThdKPYhKJJT6PI/edit?usp=sharing)
- [User testing - feedback](https://forms.gle/QTgp7166DNkaMjvv8)
- [Test plan](https://docs.google.com/document/d/1fbVkaHjzB5Xo0pqdVr2VbAr-hRv23Xvpp8Y2EXSeIC0/edit?usp=sharing)
- [Issue log](https://github.com/den01-btec-2020/text-based-adventure-Scott3142/issues)
- [Evaluation document](https://docs.google.com/document/d/1BoXYRDqdyRdLScKT-PPD2Yea0WAcmqmfjdTPzCkSVfQ/edit?usp=sharing)

The psuedo-code for the game is below:

```bash
get user name

print welcome message

set up variables

    rooms = ['N','E','S','W']
    directions = ['North','East','South','West']
    items = ['rope','tin opener','wire cutters','corkscrew']
    puzzles = ['2 + 3 = ','3 + 4 = ','5 + 6 = ','6 + 6 = ']
    answers = ['5','7','11','12']
    codes = ['rgzs','afes','wupw','pqnd']
    life_counter = 3
    my_items = []

loop until break
    get direction

    (catch invalid input)

    if room has already been entered and item collected (is item in my_items?)
        do nothing (exit to main room)
    else
        print puzzle statement
        get user answer
        if answer is correct
            append item to my_items
            print code part
        else
            decrease life by 1

    if life_counter < 1
        print endgame statement and exit program
    elseif all items are collected
        print well done statement
        ask for full code
        if code is correct
          print congratulations and exit program
        else
          decrease life by 1
        if life_counter < 1
          print endgame statement and exit program
```
