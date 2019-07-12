# Create complex multi-dimensional arrays

```
let myNestedArray = [ //level 1
  // change code below this line
  ['unshift', false, 1, 2, 3, 'complex', 'nested'], //level 2
  [
    ['loop', 'shift', 6, 7, 1000, 'method', 'deep'], //level 3
    [
      ['concat', false, true, 'deeper', 'spread', 'array'], //level 4
      [
        ['deepest', 'mutate', 1327.98, 'splice', 'slice', 'push'] //level 5
      ]
    ]
  ],
  ['iterate', 1.3849, 7, '8.4876', 'arbitrary', 'depth']
  // change code above this line
];

```

# Add Key-Value Pairs to JavaScript Objects

```
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28
};

// change code below this line
foods["bananas"] = 13
foods["grapes"] = 35
foods["strawberries"] = 27
// change code above this line

console.log(foods);

```


# Modify an Object Nested Within an Object

```

let userActivity = {
  id: 23894201352,
  date: 'January 1, 2017',
  data: {
    totalUsers: 51,
    online: 42
  }
};

userActivity.data.online = 45;

```

# Access Property Names with Bracket Notation

```
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  return foods[scannedItem];
}

```

# Use the delete Keyword to Remove Object Properties

```

let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

// change code below this line
delete foods.oranges
delete foods.plums
delete foods.strawberries
// change code above this line

console.log(foods);

```

# Check if an Object has a Property

```
let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(obj) {
  // change code below this line
   if(users.hasOwnProperty('Alan', 'Jeff', 'Sarah','Ryan'))
   {
     return true
   } else
   {
     return false
   }
  // change code above this line
}

console.log(isEveryoneHere(users));

```

# Iterate Through the Keys of an Object with a for...in Statement

```
llet users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function countOnline(obj) {
  let online = 0;
  for(let user in obj){
    if(obj[user].online == true) {
      online += 1;
    }
  }
  return online;
}

console.log(countOnline(users));

```


# Generate an Array of All Object Keys with Object.keys()


```
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function getArrayOfUsers(obj) {
  return Object.keys(users);
}

console.log(getArrayOfUsers(users));


```

# Modify an Array Stored in an Object

```
let user = {
  name: 'Kenneth',
  age: 28,
  data: {
    username: 'kennethCodesAllDay',
    joinDate: 'March 26, 2016',
    organization: 'freeCodeCamp',
    friends: [
      'Sam',
      'Kira',
      'Tomo'
    ],
    location: {
      city: 'San Francisco',
      state: 'CA',
      country: 'USA'
    }
  }
};

function addFriend(userObj, friend) {
  // change code below this line  
  userObj.data.friends.push(friend)
  return userObj.data.friends
  // change code above this line
}

console.log(addFriend(user, 'Pete'));

```

# ALGORITHMSJS

# Celsius to Fahrenheit

```

function convertToF(celsius) {
  let fahrenheit = (celsius * 1.8) + 32;
  return fahrenheit;
}
console.log(convertToF(-30))

```


# Reverse a String

```
function reverseString(str) {
  return str.split("").reverse().join();
}

```
## Second option

```
function reverseString(str) {

    var newString = "";
    for (var i = str.length - 1; i >= 0; i--) { 
        newString += str[i]; // or newString = newString + str[i];
    }

    return newString; // "olleh"
}


console.log(reverseString('hello'))


```

# Factorialize a Number


```

function factorialize(num) {
 let total = 1
  for (i=1;i<=num; i++){
        total = total * i
  }
  return total;
}

console.log(factorialize(5))



```

## My second option


```
function factorialize(num) {
  if (num < 0)
        return -1;
  else if (num == 0)
      return 1;
  else {
      return (num * factorialize(num - 1));
  }
}
console.log(factorialize(5))

```

# Find the Longest Word in a String

```

function findLongestWordLength(str) {
  var strSplit = str.split(' ');
  var longestWord = 0;
  for(var i = 0; i < strSplit.length; i++){
    if(strSplit[i].length > longestWord){
  longestWord = strSplit[i].length;
     }
}
  
  return longestWord;
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");

```
 
