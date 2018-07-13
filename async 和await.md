```javascript
function dataList () {
  return new Promise ((resolve, reject) => {
    setTimeout (() => {
      resolve(123)
    }, 5000)
  })
}

async function getData () {
  try {
    let dat = await dataList();
    return dat;
  } catch (e) {
    console.log(e)
  }
  
}
getData().then(res => { 
  console.log(res)
})
console.log('放在里面才执行')
```

