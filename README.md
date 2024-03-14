# Design Doc 
## Midterm 2024 Zachary Smith
---
## Interpreting Input:
><pre></pre>
>##### Overview
>- Access files arrivingAnimals.txt and animalNames.txt
>- Read files line by line, extracting the information
>##### arrivingAnimals.txt
>- Each line in arrivingAnimals.txt contains all the information for only one animal, with information being separated by commas
>- Read the file line by line
>- Pass that line into different functions that perform string operations to extract the needed info
>- These different "extract" functions can be re-used for each line since every line has the same formatting
>- Store the return of each of the functions in an Animal class object and push that to a vector
>##### animalNames.txt
>- animalNames.txt has a lot more empty space and unequal formatting, but contains comma-separated lists of names that coincide with each of the four species
>- Read the file line by line
>- Check if the line contains the species of the animal you want names for
>- If so, skip the line after and get the list of names, then send that to a randomization function to pick a random name for the animal
>- If not, keep checking line by line for the species


### Depositing Data:
><pre></pre>
>##### Overview
>- Create a new Animal object with the extracted info
>- Push that animal into a vector
>##### Animal Allocation
>- Animal class contains variables for name, age, species, sex, season, color, weight, and origin
>- User-defined and default constructors
>- Getters and setters for each of the variables
>- Subclasses with user-defined constructors and unique attributes
>- Unique methods / attributes are undecided. Maybe a fun fact function for each of the species or something
>##### Separating Species into Subclasses
>- Map the possible results of extractSpecies() to different function calls that return a new object of the appropriate subclass 
>- Push the new Animal into the vector
><pre></pre>
```cpp
animals.push_back(
    createAnimal[extractSpecies(line)](
        extractName(line),
        extractAge(line),
        extractSpecies(line),...
    )
)
```

### Written Report:
><pre></pre>
>##### Overview
>- Create an output txt file
>- Loop through the vector, writing a report of each animal to the file using the getter methods to retrieve the data from the object
><pre></pre>
