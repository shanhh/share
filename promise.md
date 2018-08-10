```javascript
// promise 的then 写法
function getData (type) {
	return new Promise ((resolve, reject) => {
        setTimeout(() => {
          if (type == 1) {
            resolve('成功了');
          } else {
            reject('失败了');
          }
        }, 2000)
      })
    }
    getData(2).then(res => {
      console.log(res, '1');
    }).catch(res => {
      console.log(res, '2');
    })
    // async await
    async function testFn () {
      try {
        let r = await getData(1);
        console.log(r, '3')
      } catch (e) {
        console.log(e);
      }
    } 
    testFn();

    setTimeout(() => {
      console.log('0秒的定时', '4');
    }, 0)

    setTimeout(() => {
      console.log('1秒的定时', '5');
    }, 1000)

    console.log('执行完了', '6');
```

