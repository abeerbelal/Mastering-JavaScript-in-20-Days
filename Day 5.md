# Fifth Day 🔥

## Conditionals 👩🏻‍💻

If statment: ❓🌟
If it's given some other value, JS will convert it to a boolean and decide based on its "truthiness”
```javaScript
const you = {wannaBeMyLover: true};
if (you.wannaBeMyLover) {
    you.gottaGetWithMyFriends = true;
}
```
code in the if block only runs if the (condition) is true

- we can use else to run other code if (condition) is false
```javaScript
if (you.reallyBugMe) {
    console.log("Goodbye");
} else {
    console.log("Hello");
}
```
- We can chain else and if blocks to account for multiple conditions
  ```javaScript
  function compare(x, y) {
    if (x > y) {
        console.log(x, "is greater than", y);
    } else if (x < y) {
        console.log(x, "is less than", y);
    } else {
        console.log(x, "is equal to", y);
    }```


### The (condition) is usually an expression that evaluates to a boolean
```javaScript
if (forecast === "rain") {
    console.log("bring an umbrella");
}

```

- If it's given some other value, JS will convert it to a boolean and decide based on its "truthiness" `if ("nonempty strings are truthy") {
    console.log("this line will run");
### Conditional ternary operator `condition ? valueIfTrue : valueIfFalse; `



## Loops 💫

Loops let us run the same chunk of code multiple times => this is called iteration
```javaScript
for (let rep = 0; rep < 10; rep += 1) {
    console.log("now doing rep", rep);
}
console.log("do you even lift bro");
```
We can use for...of to iterate over characters in a string 
```javaScript
for (let char of "ALOHA") {
    console.log(char);
}
```
OR items in an array ,because strings & arrays are "iterables"
```javaScript
for (let item of ["pop", 6, "squish"]) {
    console.log(typeof item);
}
```

## map & filter 🌟 
The map & filter methods also let us process all the items in an array

### map : 🗺️
Calls a function on each item in an array to create a new array
```javaScript
const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];
const nicknames = spices.map(s => s.nickname + " Spice"); //Arrow functions are useful for this!
```

> note:📌
> String templates are useful too! Make them with backticks and ${}, e.g.
> s => `${s.nickname} Spice`; is equivalent to s => s.nickname + " Spice"


### filter 
calls a true/false function on each item, and creates a new array with only the items where the function returns true
```
const mels = spices.filter(s => s.name.includes("Mel"));
```

Examp;e 🔍:
```javaScript
/* From the spices array, use map and filter to:

create a new array names with only the name of each girl
create a new array endInY with just the girls whose nickname ends in "y" */

const spices = [
    {name: "Emma", nickname: "Baby"},
    {name: "Geri", nickname: "Ginger"},
    {name: "Mel B", nickname: "Scary"},
    {name: "Mel C", nickname: "Sporty"},
    {name: "Victoria", nickname: "Posh"}
];

const names = spices.map(s=>s.name)
const endInY = spices.filter(s=>s.nickname.endsWith("y"))
```

## Spread (...): 💎
Is another neat trick for iterating over arrays,
It lets us take all the items in an array and spread 'em around


### Spread (...): 💎🔮
It lets us take all the items in an array and spread 'em around
```javaScript
const oldBurns = ["square", "wack"];
const newBurns = ["basic", "dusty", "sus"];

const burnBook = [...oldBurns, ...newBurns];
// equivalent to
const burnBook = oldBurns.concat(newBurns);
```
We can also use it to pass all the items from an array as arguments to a function or method
```
const skills = ["HTML", "CSS", "JS"];
const newSkills = ["React", "TypeScript", "Node"]
skills.push(...newSkills);
console.log(...skills);
```
## Loops ...continued
while loops
let us run a chunk of code over & over if a (condition) is true
```javaScript
let fiveRandomNumbers = [];
while (fiveRandomNumbers.length < 5) {
    fiveRandomNumbers.push(Math.random());
}
```
> Warrning ⚠️⚠️⚠️⚠️⚠️
> Don't use while (true) unless you want to see your computer burn!

## Doggo Fetch ✨✨✨
```html
<!DOCTYPE html>
<!-- saved from url=(0068)https://anjana.dev/javascript-first-steps/3-doggofetch-finished.html -->
<html lang="en-US"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    
    <title>Doggo Fetch</title>
    <style>
        body {
            margin: 1rem auto;
            padding: 3rem;
            font-family: sans-serif;
        }
        header {
            width: 70%;
            margin: 1em auto;
        }
        main {
            max-width: 70%;
            margin: 0px auto;
            display:flex; 
            flex-direction: column;
        }
        img {
            max-width: 100%;
        }
        #image-frame {
            font-size: x-large;
            text-align: center;
            margin: 1rem auto;
        }
        #explanation, #score {
            padding: 1rem;
            text-align: center;
        }
        #options {
            max-width: 100%;
            display: flex;
            flex-direction: column;
        }
        button {
            padding: 0.5rem;
            font-size: medium;
            border-radius: 5px;
        }
        .correct {
            background-color: lightgreen;
        }
        .incorrect {
            background-color: lightpink;
        }
        .hidden {
            display: none;
        }
    </style>
  </head>
  <body>
    <header>
    <h1>Guess the Doggo</h1>
    <p>What breed is the dog in this image?</p>

    </header>

    <main>
    <div id="image-frame"><img src="./Final_files/PXL_20210220_100624962.jpg"></div>
    <div id="options">
    <button name="medium poodle" value="medium poodle" class="correct">medium poodle</button><button name="australian terrier" value="australian terrier" class="incorrect">australian terrier</button><button name="french bulldog" value="french bulldog">french bulldog</button></div>

    </main>

  


  <script type="module">

    const RANDOM_IMG_ENDPOINT = "https://dog.ceo/api/breeds/image/random";

    const BREEDS = ["affenpinscher", "african", "airedale", "akita", "appenzeller", "shepherd australian", "basenji", "beagle", "bluetick", "borzoi", "bouvier", "boxer", "brabancon", "briard", "norwegian buhund", "boston bulldog", "english bulldog", "french bulldog", "staffordshire bullterrier", "australian cattledog", "chihuahua", "chow", "clumber", "cockapoo", "border collie", "coonhound", "cardigan corgi", "cotondetulear", "dachshund", "dalmatian", "great dane", "scottish deerhound", "dhole", "dingo", "doberman", "norwegian elkhound", "entlebucher", "eskimo", "lapphund finnish", "bichon frise", "germanshepherd", "italian greyhound", "groenendael", "havanese", "afghan hound", "basset hound", "blood hound", "english hound", "ibizan hound", "plott hound", "walker hound", "husky", "keeshond", "kelpie", "komondor", "kuvasz", "labradoodle", "labrador", "leonberg", "lhasa", "malamute", "malinois", "maltese", "bull mastiff", "english mastiff", "tibetan mastiff", "mexicanhairless", "mix", "bernese mountain", "swiss mountain", "newfoundland", "otterhound", "caucasian ovcharka", "papillon", "pekinese", "pembroke", "miniature pinscher", "pitbull", "german pointer", "germanlonghair pointer", "pomeranian", "medium poodle", "miniature poodle", "standard poodle", "toy poodle", "pug", "puggle", "pyrenees", "redbone", "chesapeake retriever", "curly retriever", "flatcoated retriever", "golden retriever", "rhodesian ridgeback", "rottweiler", "saluki", "samoyed", "schipperke", "giant schnauzer", "miniature schnauzer", "english setter", "gordon setter", "irish setter", "sharpei", "english sheepdog", "shetland sheepdog", "shiba", "shihtzu", "blenheim spaniel", "brittany spaniel", "cocker spaniel", "irish spaniel", "japanese spaniel", "sussex spaniel", "welsh spaniel", "english springer", "stbernard", "american terrier", "australian terrier", "bedlington terrier", "border terrier", "cairn terrier", "dandie terrier", "fox terrier", "irish terrier", "kerryblue terrier", "lakeland terrier", "norfolk terrier", "norwich terrier", "patterdale terrier", "russell terrier", "scottish terrier", "sealyham terrier", "silky terrier", "tibetan terrier", "toy terrier", "welsh terrier", "westhighland terrier", "wheaten terrier", "yorkshire terrier", "tervuren", "vizsla", "spanish waterdog", "weimaraner", "whippet", "irish wolfhound"];

    
    // Utility function to get a randomly selected item from an array
    function getRandomElement(array) {
        const i = Math.floor(Math.random() * array.length);
        return array[i];
    }

    // Utility function to shuffle the order of items in an array in-place
    function shuffleArray(array) {
        return array.sort((a,b) => Math.random() - 0.5);
    }



    // TODO 1
    // Given an array of possible answers, a correct answer value, and a number of choices to get,
    // return a list of that many choices, including the correct answer and others from the array
    function getMultipleChoices(n, correctAnswer, array) {
        // Use a while loop and the getRandomElement() function
        // Make sure there are no duplicates in the array
        const choices = [correctAnswer];
        while (choices.length < n) {
            let candidate = getRandomElement(array);
            if (choices.indexOf(candidate) < 0) { // check if this is already in the array
                choices.push(candidate); // if not, add it
            }
        }
        return shuffleArray(choices);
    }

    
    // TODO 2
    // Given a URL such as "https://images.dog.ceo/breeds/poodle-standard/n02113799_2280.jpg"
    // return the breed name string as formatted in the breed list, e.g. "standard poodle"
    function getBreedFromURL(url) {
        // The string method .split(char) may come in handy
        // Try to use destructuring as much as you can
        const [,path] = url.split("/breeds/");
        const [breedID] = path.split("/");
        const [breed, subtype] = breedID.split("-");
        return [subtype, breed].join(" ");
    }



    // TODO 3
    // Given a URL, fetch the resource at that URL, 
    // then parse the response as a JSON object,
    // finally return the "message" property of its body
    async function fetchMessage(url) {
        const response = await fetch(url);  // Fetch the resource at the given URL
        const {message} = await response.json(); // Parse the response as JSON & remember its 'message' value
        return message; // Return the message
    }


    // Function to add the multiple-choice buttons to the page
    function renderButtons(choicesArray, correctAnswer) {

        // Event handler function to compare the clicked button's value to correctAnswer
        // and add "correct"/"incorrect" classes to the buttons as appropriate
        function buttonHandler(e) {
            if (e.target.value === correctAnswer) {
                e.target.classList.add("correct");
            } else {
                e.target.classList.add("incorrect");
                document.querySelector(`button[value="${correctAnswer}"]`).classList.add("correct");
            }
        }

        const options = document.getElementById("options"); // Container for the multiple-choice buttons

        // TODO 4
        // For each of the choices in choicesArray,
        // Create a button element whose name, value, and textContent properties are the value of that choice,
        // attach a "click" event listener with the buttonHandler function,
        // and append the button as a child of the options element
        choicesArray.map(choice => {
            let button = document.createElement("button");
            button.value = button.name = button.textContent = choice;
            button.addEventListener("click", buttonHandler);
            options.appendChild(button);
        })
    }


    // Function to add the quiz content to the page
    function renderQuiz(imgUrl, correctAnswer, choices) {
        const image = document.createElement("img");
        image.setAttribute("src", imgUrl);
        const frame = document.getElementById("image-frame");

        image.addEventListener("load", () => {
            // Wait until the image has finished loading before trying to add elements to the page
            frame.replaceChildren(image);
            renderButtons(choices, correctAnswer);
        })
        
    }

    // Function to load the data needed to display the quiz
    async function loadQuizData() {
        document.getElementById("image-frame").textContent = "Fetching doggo...";
        
        const doggoImgUrl = await fetchMessage(RANDOM_IMG_ENDPOINT);
        const correctBreed = getBreedFromURL(doggoImgUrl);
        const breedChoices = getMultipleChoices(3, correctBreed, BREEDS);

        return [doggoImgUrl, correctBreed, breedChoices];
    }

    // TODO 5
    // Asynchronously call the loadQuizData() function,     
    // Then call renderQuiz() with the returned imageUrl, correctAnswer, and choices 
    const [imageUrl, correctAnswer, choices] = await loadQuizData();
    renderQuiz(imageUrl, correctAnswer, choices);
    


  </script>

</body></html>
```


## (A)synchronous code✨🎀

JS can usually run straight through our program "synchronously"(line after line)

Some things that take time:💡

- Waiting for user events
- Asking a user to pick a file
- Getting permission to access the camera/mic
- Loading data from the interwebs

So when we give JS a task that takes a while, it doesn't stop and wait
```javaScript
console.log("This will print first");
setTimeout(() => console.log("This will print third"), 1000);
console.log("This will print second");
```

it adds the slow task to a "TODO list" and keeps on running our program

The task runs some time later, "asynchronously"
