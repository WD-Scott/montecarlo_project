# Monte Carlo Package:

## Metadata:
Wyatt Scott's Final Project (Monte Carlo Simulator)


## Synopsis:
...

### Installing:
``!pip install .``
### Importing: 
``from montecarlo import Die, Game, Analyzer``

### Creating dice:
- Object:
- Change Weight:
- Roll:

### Playing games:
- Begin Game:
- Play:
- Show Results:

### Analyzing games:
- Start Analyzer:
- Face Counts per Roll:
- Jackpot:
- Combo:

### Classes and attributes:

### Die Class:
A die class with N sides/faces and W weights that can be rolled to select a side/face.
#### Attributes:
- None
#### Methods:
##### ``__init__``:
Initializer that takes an array or list of faces of any length, initializes weights to 1, then saves to a private dataframe.
###### Parameters:
- faces
##### ``weight_change``:
A method that changes a side/face weight and checks whether side/face and weight are valid.
###### Parameters:
- face
- weight_changed
##### ``rolls``:
A method that rolls the die one or more times but defaults to 1. Returns a list of outcomes.
###### Parameters:
- rolls
##### ``show_faces_weights``:
A method that shows the dataframe of faces and weights.
###### Parameters:
- None


### Game Class:
A game class that consists of rolling of one or more dice of the same kind one or more times.
#### Attributes:
- None
#### Methods:
##### ``__init__``:
Initializer that takes a single parameter, a list of already instantiated similar Die objects.
###### Parameters:
- die_list
##### ``play``:
A method that takes a parameter to specify how many times the dice should be rolled. Saves the result of the play to a private dataframe of shape N rolls by M dice. Results in a table of data with columns for: 
- roll number
- the die number (its list index)
- the face rolled in that instance
###### Parameters:
- rolls
##### ``show``:
A method that shows the user the results of the most recent play. Takes a parameter to return the dataframe in narrow or wide form. This parameter defaults to wide form. This parameter raises an exception if the user passes an invalid option. The narrow form of the dataframe will have a two column index with:
- the roll number
- the die number
- a column for the face rolled
The wide form of the dataframe will be a single column index with:
- the roll number
- each die number as a column


### Analyzer Class:
#### Attributes:
- None
#### Methods:
##### ``__init__``:
Initializer that takes a game object as its input parameter. At initialization time, it also infers the data type of the die faces used.
###### Parameters:
- game
##### ``face_counts_roll``:
A method that computes how many times a given face is rolled in each event. Stores the results as a dataframe in a public attribute. The dataframe has an index of the roll number and face values as columns (i.e. it is in wide format).
###### Parameters:
- None
##### ``jackpot``:
A method that computes how many times the game resulted in all faces being identical. Returns an integer for the number times to the user. Stores the results as a dataframe of jackpot results in a public attribute.
###### Parameters:
- None
##### ``combo``:
A method that computes the distinct combinations of faces rolled and their counts. Combinations are sorted and saved as a multicolumned index. Stores the results as a dataframe in a public attribute.
###### Parameters:
- None

## Manifest:

### Files in repo:
- montecarlo_demo.ipynb
- montecarlo_test.py
- montecarlo.py
- setup.py
- 
