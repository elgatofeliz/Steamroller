# Steamroller

FreeCodeCamp
Steamroller

Flatten a nested array. You must account for varying levels of nesting.

### Code

function steamrollArray(arr) {
  let result = []

  function check (val){
    val.forEach(elt => {
      if(!Array.isArray(elt)){
        result.push(elt)
      }
      if(Array.isArray(elt)){
        check(elt)
      }
    })
  }
  
  check(arr)
  return result
}

steamrollArray([1, [2], [3, [[4]]]]);
