## File cleaner
Read a file, remove all the extra spaces and write it back to the same file.

For example, if the file input was
```
hello     world    my    name   is       raman
```

After the program runs, the output should be

```
hello world my name is raman
```

const fs = require('fs');

const filePath = 'a.txt';

function cleanData(data){
  var arr = data.split(" ");
  console.log(arr)
  let cleanedData = []
  for (let i=0;i<arr.length;i++){
    if(arr[i].length !== 0){
      cleanedData.push(arr[i])
    }
  }
  let cleanedDataString = cleanedData.join(" ")
  console.log(cleanedDataString)
  return cleanedDataString
  
}
const readedData = fs.readFileSync(filePath, 'utf8');
let finalData=cleanData(readedData)
fs.writeFile(filePath,finalData,'utf8',(err) => {
  if (err) {
    console.error('Error writing to the file:', err);
    return;
  }
  console.log('Content written to the file successfully.');
});

