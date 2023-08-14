## Counter without setInterval

Without using setInterval, try to code a counter in Javascript. There is a hint at the bottom of the file if you get stuck.

let counter = 0

function count(){
  console.clear()
  counter+=1
  console.log(counter)
    
 setTimeout(count,1*1000)
}

setTimeout(count,1*1000)






































































(Hint: setTimeout)
