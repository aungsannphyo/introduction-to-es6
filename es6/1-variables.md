### Variables

#### 1. Var

ပုံမှန်အားဖြင့် Vanilla Javascript မှာ variables ကြော်ငြာတဲ့အခါ var ဆိုတဲ့ keyword ကိုအသုံးပြုကြတယ်။

`Example - 1`

​	

```javascript
	var counter = 5;

​		console.log(counter);	Answer => 5

​		var counter =  10;

​		console.log(counter);	Answer => 10
```



`Example - 2`

```javascript
		var counter = 5;

​		console.log(counter);	Answer => 5

​		counter =  10;

​		console.log(counter);	Answer => 10
```





အပေါ်က example ၁ နဲ့  ၂ မှာ var အသုံးပြုပုံကို ပြောပြထားတာဖစ်တယ်။ example ၁  မှာဆိုရင် counter ဆိုပီး variable ကြော်ငြာပီး  5 ကို assign လုပ်လိုက်တယ် ပီးတော့ နောက်အဲ့နာမည်တိုင်းပဲ ကြော်ငြာပီး 10 ကို assign  ထပ်လုပ်တယ် အဲ့တော့ပထမတစ်ခုကို overwrite ဖစ်သွားပီး နောက်ဆုံးမှာ အဖြေက 10 ဖစ်သွားတယ် ။  variable name တူတူ နှစ်ခါ declare  လုပ်တာကို error တက်မသွားပဲ အဖြေရတော့  ကိုယ့် Project  မှာ var keyword  ကိုသုံးပီး ရေးတဲ့အခါတိုင်ပတ်တဲ့အချိန်တွေရှိနိုင်ပီး နည်းနည်း messy ဖစ်တယ်။ example 2 မှာလဲ လုပ်ငန်းပုံစံက တူတူပေမဲ့ declare လုပ်ထားတဲ့  counter ထဲ ကိုပဲ overwrite ထပ်လုပ်ပီး နောက်ဆုံး အဖြေက  10 ဖစ်သွားတယ်။

var ကို scoped variable or globally variable အနေနဲ့သုံးလို့ရတယ်။

`Example - 3`

```javascript
var counter = 5;

function sayName() {

​	console.log(counter);

​	var name = "Batman";

​	console.log(name);

}

sayName();	

Answer =>	5,Batman

console.log(name)

ReferenceError: name is not defined
```

Example 3 မှာဆိုရင် counter က global variable ဖစ်ပီး name  က scope variable ဖစ်တယ်။ scope variable ဆိုတာသူသတ်မှတ်ထားတဲ့အပိုင်းထဲမှာပဲသုံးခွင့်ရှိတာကိုပြောချင်တာဖစ်တယ် အာ့ကြောင့်  console.log(name)  ဆိုပီး  { }  အပြင်ကနေ name ကိုအဖြေထုတ်ကြည့်တဲ့အခါ error တက်သွားတာကိုတွေ့ရလိမ့်မယ်။ 



#### 2 . Let  

let and const keyword တွေက ES6 မှ စတင်ပါ၀င် လာတာဖစ်ပီး  ES6 ဆိုတာက ၂၀၁၅ မှာ ဖန်တီးခဲ့တဲ့ အတွက် ECMAScript 2015 or ECMAScript 6 လို့ခေါ်ကြတယ်။ သူကဘာတွေလုပ်ဆောင်ပေးသလဲဆိုရင် လက်ရှိ Javascript (ES5) မှာအသုံး၀င်တဲ့ လုပ်ဆောင်ချက်ပေါင်းများစွာကို အဆင့်မြှင့်ပီး ပို၍လွယ်ကူအောင်  easier for devs to code လို့ရအောင်လုပ်ဆောင်ပေးထားတာဖစ်တယ်။ React ကျရင်လဲ  ES6   ကိုပဲ အဓိက ထားသုံးမှာမို့ မဖစ်မနေသိထားရမဲ့ အရာတစ်ခုဖစ်တဲ့အတွက် သေချာကြည့်ထားဖို့လိုမယ်ဗျ။ ကဲ အာ့ဆို  let keyword usage ကြည့်လိုက်ရအောင် ...

`Example - 4` 

```javascript
let name = "Batman"

console.log(name);	Answer  => Batman
```



သူ့ကိုအသုံးပြုပုံကလဲ var နဲ့တူတူပဲ ပီးတော့အပေါ်က var လို သူကလဲ global and scoped variable ဖစ်တယ် အသုံးပြုပုံကလဲ var နဲ့တူတူပဲဖစ်တယ် ။ 

`Example - 5`

```javascript
let counter = 5;

function sayName() {

​	console.log(counter);

​	let name = "Batman";

​	console.log(name);

}

sayName();

Answer => 5,Batman

console.log(name)

ReferenceError: name is not defined
```



ကဲ အဲ့ဒါဆို variable name တူတူပေးပီး သုံးကြည့်ရအောင်

`Example - 6`

```javascript
let name = "Batman"

let name = "Superman"

console.log(name);	

Error =>  SyntaxError: Identifier 'name' has already been declared
```



example 6 မှာအပေါ်က var လို variable name တူတူ let keyword ကိုသုံးပီး declare လုပ်တဲ့ချိန်မှာဆို error တက်တယ်။ အဲ့တော့ ကျွန်တော်တို့က var ကိုမသုံးသင့်တော့ဘူး ဘာလို့ဆိုအပေါ်မှာပြောခဲ့သလို တိုင်ပတ်နိုင်လို့  var အစား  let keyword ကိုပဲ သုံးသင့်တယ်။ ဘာလိုအခြေအနေတွေမှာတိုင်ပတ်နိုင်သလိုဆိုတာကို ကျွန်တော် example code နဲ့အောက်မှာရှင်းပြပါမယ်။ 

`Example - 7`

```javascript
let numberList = [1, 2, 3, 4, 5];

for (var i = 0; i < numberList.length; i++) {

console.log("inside looping", i);

​	***Answer => 0 , 1, 2, 3, 4***

}

console.log("outside looping", i)

**Answer =>  5**
```



example 7 မှာ var ကို သုံးပီး loop ပတ်လိုက်တဲ့ ချိန်မှာ inside looping  ထဲရော  outside looping  ထဲမှာရောအဖြေတွေရနေတာတွေ့ရလိမ့်မယ်။ တကယ်လိုကိုယ်က i ကိုနောက်ထပ် variable အနေ အခုလိုနဲ့ declare လုပ်ပီးထပ်သုံးမိရင်တိုင်ပတ်ပီ။ အဲ့နေရာမှာ ဖစ်သင့်တာက let keyword  ပဲ ဖစ်သင့်တယ်။

`Example - 8`

```javascript
let numberList = [1, 2, 3, 4, 5];

 for (let i = 0; i < numberList.length; i++) {

	console.log("inside looping", i);

 }
	console.log("outside looping", i)

 Error => ReferenceError: i is not defined


```



#### 3. Const

const ကတော့ တစ်ကြိမ်ပဲ assign လုပ်ခွင့်ရှိတယ် အပေါ်က var and let လိုပြန်ပီး assign လုပ်ပိုင်ခွင့်မရှိဘူး။ သူ့ကိုသုံးချင်ရင် စပီး declare  လုပ်ကတဲက တခါထဲ assign လုပ်ပေးရတယ်။ သူ့ကို declare လုပ်ရင် Lowercase နေနေ  Uppercase နေနေကြိုက်သလို declare လုပ်လို့ရပေမဲ့ များသောအားဖြင့်အကြီးနဲ့ပဲ ရေးကြတယ်။ သူကလဲ global အနေနဲ့ရော scoped အနေနဲ့ရောသုံးလို့ရတယ်။ const  ကိုဘယ်လိုနေရာတွေမှာသုံးလဲဆိုရင် အသေထားရမဲ့အရာတွေ ပြောင်းလဲမှု့မရှိတဲ့ကောင်တွေမှာသုံးကြတယ် example အနေနဲ့  api route တွေမှာသုံးလေ့ရှိတယ်

> const api = "www.example.com/api/v1";

အဲ့လိုကြော်ငြာပီး api ဆိုတဲ့ variable ကို နေရာတိုင်းကနေခေါ်သုံးလို့ရတယ်..

`Example - 9 `

```javascript
const NAME;

NAME = "batman"

console.log(NAME)

**Error => Missing initializer in const declaration**

const NAME = "Batman"

console.log(NAME)

**Answer => Batman**
```



