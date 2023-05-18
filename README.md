# Mod2 Week2 Assessment - Braden Smith

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
*Test Driven Development is the process of creating tests before classes and methods. I think of it as setting guidelines for yourself, helping you lay out exactly what is needed at each step.

1. What are three benefits of using TDD?
*Setting a guideline with all necessary elements, before adding methods.
*You're able to take your time going error by error until you're in the green. This will get your program working, and you can refactor later.
*When writing tests first, you're forced to code in small pieces, but this helps you stay organized throughout development.

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
*I use test-driven development to set a rigid logic guidline for my tests. By using TDD, I am able to break up my code into small bite-size pieces that helps me understand where and why I need each
element that I am adding to my project.

1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

I would remove this one and replace it with 'Dog_Constructor...' to test that all properties are assigned correctly not just name.
[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}

[Fact]
public void Dog_Constructor_SetsCorrectPropertyValues()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.True(dog.IsHungry);
    Assert.Equal("Nile", dog.Name);
    Assert.Equal("Golden Retriever", dog.Breed);
}

[Fact]
public void Dog_Eat_SetsIsHungryFalse()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat();

    Assert.False(dog.IsHungry);
}

[Fact]
public void Dog_Sleep_SetsIsHungryTrue()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Sleep();

    Assert.True(dog.IsHungry);
}
```

5. What is a merge conflict, and when might you encounter one?
*A merge conflict is when you are attempting to merge a branch into main where both branches have code on the same line(s) in the file(s).

1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
*The order in which we merge does not matter as long as we don't do it at the same time as this would be very confusing with merge conflicts. When one person finishes, lets say aa-branch, they can create
a pull request. Once this is done I would go to GitHub and review the PR and resolve any conflicts, give feedback, or merge. Then once bb-branch is done we do the same process, just reveresed roles.

1. Why is it good practice to have someone else approve and/or merge your PR?
*Prof T: "You never want to add code to a project without your team knowing". A teammember also might catch a bug that was overlooked, they might be able to refactor, or it just simply needs adjustments.
If you were to just merge your own PR you would be skipping a critical step in the process.
  
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
