function dropElements(arr, func) {
  let result = []; 

  for(let i=0; i<arr.length; i++) {
    if(func(arr[i])) {
      result = arr.slice(i);
      break;
  }
  }

  return result;
}

//test
//dropElements([1, 2, 3, 4], function(n) {return n >= 3; });
//dropElements([0, 1, 0, 1], function(n) {return n === 1;});