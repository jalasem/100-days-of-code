# My FCC Bonfire Solutions


### Reverse String

**Solution**
--------------
```
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```

### Factorialise a number

**Solution**
--------------

```
function factorialize(num) {
  var factorial = 1;
  for(var i = 2; i <= num; i++){
    factorial = factorial * i;
  }
  return factorial;
}

factorialize(5);
```

### Palindrome

**Solution**
--------------
```
function palindrome(str) {
  // Good luck!
  var straight = str.replace(/[\W_]/g, '').toLowerCase();
  var reversed = str.replace(/[\W_]/g, '').toLowerCase().split('').reverse().join('');
  console.log(straight, reversed);
  if(straight === reversed){
    return true;
  } else {
    return false;
  }
}

palindrome("eye");
```

### Find the longest Word

**Solution**
--------------
```
function findLongestWord(str) {
  var broken = str.split(' ');
  var longest = broken[1];
  for (var i = 0; i < broken.length; i++) {
    if(broken[i].length >= longest.length) {
      longest = broken[i];
    }
  }
  return longest.length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

**or**

```
function findLongestWord(str) {
  return str.split(' ').sort(function(a,b){
    return b.length - a.length;
  })[0].length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

### Title Case

**Solution**
--------------
```
function titleCase(str) {
  str = str.toLowerCase().split(' ');
  for(var i = 0; i < str.length; i++){
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  return str.join(' ');
}

titleCase("I'm a little tea pot");
```

**or**

```
function titleCase(str) {
  return str.toLowerCase().split(' ').map(function(word) {
    return (word.charAt(0).toUpperCase() + word.slice(1));
  }).join(' ');
}
titleCase("I'm a little tea pot");
```

### Find Largest of Four

**Solution**
--------------
```
function largestOfFour(arr) {
  // You can do this!
  var results = [];
  for(var i = 0; i < arr.length; i++) {
    var largest = 0;
    for(var j = 0; j < arr[i].length; j++){
      if(arr[i][j] > largest){
		largest = arr[i][j];
      }
    }
   results[i] = largest;
  }
  return results;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### Repeatinf String n-times

**Solution**
--------------
```
function repeatStringNumTimes(str, num) {
  // repeat after me
  var newStr = '';
  for(i = 0; i < num; i++) {
    newStr += str;
  }
  return newStr;
}

repeatStringNumTimes("abc", 3);
```

