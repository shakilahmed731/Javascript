# Javascript
Javascript Education


## Encapsulation
fancy way of saying objects
  const user1 = {
    score = 
    
function definition when you want to say it precisely

Object.create
  const user3 = Object.create(null); // null makes it a empty object
  // will evaluate into an empty object
  
  `user3.name = "Eva";
  user3.score = 9;
  user3. increment = function () {
    user3.score++;
  };`
  
function userCreator(name, score){
  const newUser = {};
  newUser.name = name;
  newUser.score = score;
  newUser.increment = function (){
    newUser.score++;
  };
  return newUser;
};

const user1 = userCreator("Will", 3);
const user2 = userCreator("Tim", 5);
user1.increment()

// the arguments in the function become variables in the local execution context

# Using the prototype chain

const functionStore = {
  increment: function (){this.score++;}.
  login: function(){console.log("You're loggedin")}
};

const user1 = {
  name: "Will",
  score: 3
}

## full solution
### this is a constructor function
### what is construction function?
function userCreator (name, score) {
  const newUser = Object.create(functionStore);
  newUser.name = name;
  newUser.score = score;
  return newUser;
};

const functionStore = {
  increment: function(){this.score++;),
  login: function(){console.log("You're loggedin");}
};

const user1 = userCreator("Will", 3);
const user2 = userCreator("Tim", 5);
user1.increment();

// this <-- its evaluated at runtime
only has meaning when its invoked.


function UserCreator(name,score) {
  this.name = name;
  this.score;
};

UserCreator.prototype.increment = function (){
  this.score++;
};

UserCreator.prototype.login = function(){
  console.log("login");
};

const user1 = new UserCreator("Eva", 9)

user1.increment();

// how does the `new` keyword work in javascript? <-- interview question

now all this into a `class`

class UserCreator {
  constructor (name, score){
    this.name = name;
    this.score = score;
  }
  increment(){
    this.score++;
  }
  login(){
    console.log("login");
  }
}
const user1 = new UserCreator("Eva", 9);

user1.increment();

//hard parts challenge code
https://codesmith.io/apply/9340
