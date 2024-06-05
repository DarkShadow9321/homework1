練習題目
```js

第一題:
const myfunction= () => {
    const a = 1;
    const b = 2;
    const c = 3;
    console.log(`a是:${a} b是${b} c是:${c}`);
};
myfunction();
```
```js
第二題:
function print(number){
  if(number>0){
    console.log("正數");
  }
  else if(number===0){
    console.log("零");
  }
  else{
    console.log("負數");
  }
}
print(2)
```
```html
第三題:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p {
            color: black;
        }

        @media screen and (min-width: 350px) {
            p {
                color: blue;
            }
        }

        @media screen and (min-width: 1024px) {
            p {
                color: red;
            }
        }
    </style>
    //用此方式所有屬於<p>的文字皆會變換顏色
</head>
<body>
    <p>我的網頁</p>
</body>
</html>
```
```html
第四題:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <img id='img' src="https://fakeimg.pl/150x130" />
    <button id='bt1'>顯示圖片</button>
    <button id='bt2'>隱藏圖片</button>
    <script>
        const img =
            document.getElementById('img');
        //將button用id的方式命名可以針對特定按鈕進行設定
        const bt1 =
            document.getElementById('bt1');
        const bt2 =
            document.getElementById('bt2');
        bt1.onclick = () => {
            img.style.display = 'block';
        };
        bt2.onclick = () => {
            img.style.display = 'none';
        };
    </script>
</body>
</html>
```
```html
第五題:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h3 id=wd>我的網頁</h3>
    <button id='bt1'>黑</button>
    <button id='bt2'>藍</button>
    <script>
        const wd =
            document.getElementById('wd');
        const bt1 =
            document.getElementById('bt1');
        const bt2 =
            document.getElementById('bt2');
        bt1.onclick = () => {
            wd.style.color = 'black';
        };
        bt2.onclick = () => {
            wd.style.color = 'blue';
        };
    </script>
</body>
</html>
```
```js
第六題:
const printTree = (treeHeight, treeGap) => {
  let ans = "";
  for (let i = 0; i < treeHeight; i++) {
    let star = '*'.repeat(1 + treeGap * i);
    let dash = '-'.repeat((treeGap * (treeHeight - 1) - (star.length - 1)) / 2);
    ans +=  dash + star + dash + '\n';
  }
  return ans;
}
const treeHeight = 7;
const treeGap = 4;
console.log(printTree(treeHeight, treeGap));
```
```js
延伸題目:
第一題:
const print = (x) => x % 2 === 0 ? `${x}是2的倍數` : `${x}不是2的倍數`;
console.log(print(4));
console.log(print(7));
```
```js
第二題:
const demo = (arr, index) => {
  arr.splice(index, 1); //從arr中刪除一個index
  return arr;
}
console.log(demo(['a', 'b', 'c'], 2));
```
```html
第三題:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="date"></div>
    <script>
        const convertDate = (dateString) => {
            const date = new Date(dateString);
            //取得4位數的年份，不使用getYear()是因為返回的值會減去1990，會產生千年蟲的問題(千年蟲是指電腦無法判斷1900和2000的差別而產生的錯誤，因為顯示的結果皆為00)
            const Year = date.getFullYear() - 1911;
            //取得月份(0~11)，但因與1~12月份不同，因此需要加1，並使數字維持二位數
            const month = String(date.getMonth() + 1).padStart(2, '0');
            //取得日期，並使數字維持二位數
            const day = String(date.getDate()).padStart(2, '0');
            return `${Year}/${month}/${day}`;
        };
        const originalDate = "2024-05-23 00:00:00";
        const convertedDate = convertDate(originalDate);
        document.getElementById('date').textContent = convertedDate;
    </script>
</body>
</html>
```
```js
第四題:
const fruits = {
  Banana: {
    num: "一串",
    price: "50"
  },
  Orange: {
    num: "五顆",
    price: "100"
  },
  Apple: {
    num: "3顆",
    price: "50"
  }
};
//使用object獲取fruits中的所有物件，並使用forEach提取fruit中的內容
Object.keys(fruits).forEach(fruit => {
  const { num, price } = fruits[fruit];
  console.log(`${fruit}是${num}${price}元`);
});
```
```js
第五題:
for (let i = 1; i <= 9; i++) {
  let row = '';
  for (let j = 1; j <= 9; j++) {
    //將result的結果轉為字串並將結果以0補足為二位數
    const result = (i * j).toString().padStart(2, '0');
    row += `${i}x${j}=${result}\t`;
  }
  console.log(row);
}

```

