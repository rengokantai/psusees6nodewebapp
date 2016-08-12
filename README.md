#### psusees6nodewebapp
######20
const is scoped, like let.
```
const a=1
console.log(a); //1
if(true){
const a=2; //can be changed in another scope.
console.log(a); //2
}
```

######25
example code
```
function *book(num){
  var list=[1,2,3,4,5,6];
  var out =[];
  for( let item of list){
    out.push(item);
    if(out.length>=num){
      	num = yield out;
      	out=[];
    }
  }
  //return list;
  yield out;
  
}

var test = book(2)
console.log(test.next());
console.log(test.next(2));
console.log(test.next(3));

console.log(test.next(3));
```
