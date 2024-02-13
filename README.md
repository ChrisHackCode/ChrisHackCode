// Define arrays for each category
const vehicles = ["car", "bike", "plane", "boat", "train"];
const seaAnimals = ["fish", "dolphin", "shark", "whale", "octopus"];
const landAnimals = ["dog", "cat", "lion", "elephant", "horse"];
const shelters = ["house", "apartment", "tent", "cabin", "igloo"];
const foods = ["pizza", "burger", "pasta", "sushi", "ice cream"];

// Function to randomly select an item from an array
function getRandomItem(array) {
  return array[Math.floor(Math.random() * array.length)];
}

// Function to start the game
function startGame() {
  // Select a random item from each category
  const vehicle = getRandomItem(vehicles);
  const seaAnimal = getRandomItem(seaAnimals);
  const landAnimal = getRandomItem(landAnimals);
  const shelter = getRandomItem(shelters);
  const food = getRandomItem(foods);
  
  // Prompt the user to guess the object
  const userGuess = prompt(`Guess the object:\n1. Vehicle: ${vehicle}\n2. Sea Animal: ${seaAnimal}\n3. Land Animal: ${landAnimal}\n4. Shelter: ${shelter}\n5. Food: ${food}`);
  
  // Check if the user's guess matches any of the selected objects
  if (userGuess !== null) {
    const lowercaseUserGuess = userGuess.toLowerCase();
    if (lowercaseUserGuess === vehicle.toLowerCase() || 
        lowercaseUserGuess === seaAnimal.toLowerCase() || 
        lowercaseUserGuess === landAnimal.toLowerCase() || 
        lowercaseUserGuess === shelter.toLowerCase() || 
        lowercaseUserGuess === food.toLowerCase()) {
      alert("Congratulations! You guessed correctly!");
    } else {
      alert("Sorry, your guess is incorrect.");
    }
  }
}

// Start the game
startGame();
