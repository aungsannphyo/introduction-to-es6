## Map, Filter, Reduce

#### 1.Map

`Example - 1`

```javascript
let superHero = ["batman", "superman", "flash", "wonder woman"];

superHero.forEach((hero) => {
    console.log(hero)
});

Answer => batman,superman,flash,wonder woman
```

Example  - 1 မှာဆိုရင်ကျွန်တော်တို့အရင်က Javascript မှာ Array ကို forEach method သုံးပီး Array ထဲက Data တွေကိုပြန်ထုတ်ထားတယ်။ ပုံမှန် Javascript ပဲ ဟုတ်ပီ ES6 မှာပါလာတဲ့ map ကိုသုံးပီးရေးကြည့်ရအောင်..

`Example - 2`

```javascript
let superHero = ["batman", "superman", "flash", "wonder woman"];

let newHero = superHero.map(hero => "DC " + hero)

console.log(newHero);

Answer => [ 'DC batman', 'DC superman', 'DC flash', 'DC wonder woman' ]

console.log(superHero);

Answer => [ 'batman', 'superman', 'flash', 'wonder woman' ]
```

map() Function ကဘယ်လိုအလုပ်လုပ်သလဲဆိုရင် ပေးလိုက်တဲ့ Array ပေါ်မူတည်ပီး အခြား Array တစ်ခုကိုပြန်ပေးတဲ့ Function တစ်ခုဖစ်တယ်။ပြောရရင် အ‌ပေါ်က example -2 မှာဆိုရင် superHero ဆိုတဲ့ မူလ Array လဲတန်ဖိုးကိုလုံး၀မပြောင်းလဲပဲ  newHero ဆိုတဲ့ Array အသစ်ထုတ်ပေးလိုက်တာဖစ်တယ်ဗျ။ ဒီလို Callback Function တွေပေါ်မူတည်ပီးအလုပ်လုပ်တဲ့ ဒီလိုရေးထုံးက Functional Programming ကနေလာပါတယ်။ Functional Programming အကြောင်းသိချင်ရင် ကွကိုယ်စာဖတ်ကြည့်စေလိုပါတယ်။ နောက်ပိုင်း Array တွေကို ကိုင်တွယ်ဖို့အတွက် for , for-in, forEach တို့လို loop တွေမသုံးသင့်ပဲ map() ကိုပဲသုံးဖို့အကြုံပေးပါတယ်။ ရေးနည်းအနေနဲ့ရော နားလည်ရလွယ်ပီး code ကပိုကျစ်လစ်သွားလို့ပါ။

#### 2.Filter

`Example - 3`

```javascript
let superHero = ["batman", "superman", "flash", "wonder woman"];

let result = []
for (hero in superHero) {
    if (superHero[hero] !== "superman") {
        result.push(superHero[hero])
    }
}
console.log(result)
Answer => [ 'batman', 'flash', 'wonder woman' ]
```

Example 3 မှာဆိုရင် superHero Array ထဲက superman နဲ့မတူတဲ့ hero တွေကိုယူမယ်ဆိုတဲ့ condition တစ်ခုပါပဲ သာမာန်ကျွန်တော်တို့သိနေကြ Javascript အသုံးပြုပုံပါပဲ။ အဲ့တာကို filter() Function သုံးပီးဘယ်လိုရေးရလဲဆိုရင်...

`Example - 4`

```javascript
let superHero = ["batman", "superman", "flash", "wonder woman"];

let newHero = superHero.filter(hero => hero !== "superman")

console.log(newHero)

Answer => [ 'batman', 'flash', 'wonder woman' ]
```

Example 4 မှာဆိုရင်  filter() Function ကိုသုံးပီးရေးလိုက်တဲ့ အချိန်မှာ code ကပိုကျစ်လစ်သွားတယ်။ သူကလဲ map() လိုအလားတူ new Array တစ်ခုကိုပြန်ပေးတာဖစ်ပါတယ်။ တစ်ခုရှိတာက map လိုရှိသမျှအားလုံးပြန်ပေးတာမဟုတ်တော့ပဲ condition နဲ့ကိုက်ညီတဲ့ အရာတွေကိုသာပြန်ပေးတာဖစ်တယ်ဗျ။ အပေါ်က example 4  ကိုကြည့်ရင်နားလည်မယ်ထင်ပါတယ်။ 

#### 3.Reduce

reduce() Function က Array တစ်ခုရှိတယ် အဲ့ Array ပေါ်အခြေခံပီး တန်ဖိုးတစ်ခုကိုပဲ ပြန်ပေးပါတယ်။ အရှင်းလင်းဆုံးမြင်သာအောင်ပြောရမယ်ဆိုရင် ဥပမာ ။ ။ ငှက်ပျောသီး စပျစ်သီး ပန်းသီး သုံးခုပါတဲ့ Array တစ်ခုရှိတယ်အဲ့ Array ကို reduce() Function ဆိုတဲ့ဖျော်ရည်စက်ထဲထည့်လိုက်ရင်  ရလာမဲ့ အဖြေက သီးစုံဖျော်ရည်ဆိုတာရလာမယ် ဟဲဟဲ :smile:။ ပိုရှင်းသွားအောင် example နဲ့ကြည့်လိုက်ရအောင်...

`Example - 5`

```javascript
const numbers = [1, 2, 3, 4];

let sum = 0;
for(let n of numbers){
	sum += n;
}
console.log(sum) // => 10
```

 အပေါ်က example 5 မှာဆိုရင် ကျွန်တော်တို့သိနေကြအတိုင်း numbers array ကို loop ပတ်ပီး sum ထဲကိုပေါင်းပေါင်းထည့်လိုက်တယ်နောက်ဆုံးမှာ အဖြေရသွားတယ်။အာ့ဆို reduce သုံးပီးရေးကြည့်လိုက်ရအောင်

`Example - 6`

```javascript
const numbers = [1, 2, 3, 4];

let sum = numbers.reduce((accumulator, currentValue) => {
    return accumulator + currentValue 
	}, 0)

console.log(sum) // => 10
```

Example 6 မှာဆို reduce() function မှာ parameter 2 ခုလိုတယ်ပထမတစ်ခုက callback function တစ်ခုရယ် နောက်တစ်ခု accumulator တန်ဖိုးရယ်။ accumulator ကဘာလဲဆို example 5 မှာ ရေးခဲ့တဲ့ sum ဆိုတဲ့ variable ကိုပြောချင်တာဖစ်ပီး ဒုတိယ parameter အတွက် 0 တန်ဖိုးက initialize လုပ်တဲ့သဘောပါပဲ ပြောရရင်  let sum = 0 လို့ကြော်ငြာလိုက်တာနဲ့တူတူပါပဲ။ currentValue ဆိုတာကတော့ array ထဲက တန်ဖိုးတွေကိုဆိုလိုတာဖစ်တယ်။

a = 0 ,  c = 1,   a + c = 1

a = 1,  c = 2,   a + c =  3

a = 3 ,  c = 3,  a + c = 6

a = 6,   c = 4,   a + c  = 10

ဒါကိုကြည့်ရင်နားလည်မယ်ထင်ပါတယ်။ အဲ့လိုမရေးချင်ရင်နောက်တစ်နည်းရေးလိုရပါသေးတယ်။

`Example - 7`

```javascript
const numbers = [1, 2, 3, 4];

let sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue);

console.log(sum) // => 10
```

Example 7 မှာဆိုရင် accumulator တန်ဖိုးမပေးတော့ပဲတစ်ကြောင်းထဲနဲ့ပီးသွားတာမြင်ရပါတယ်။ သူကကျဘယ်လိုအလုပ်လုပ်သလိုဆိုရင်

a = 1,  c = 2,   a + c =  3

a = 3 ,  c = 3,  a + c = 6

a = 6,   c = 4,   a + c  = 10

accumulator တန်ဖိုးပေးမထားတဲ့အတွက် numbers array ရဲ့ပထမဆုံးခန်းကောင်က accumulator တန်ဖိုးအနေနဲ့၀င်သွားပီးကျွန်တော်တို့မျှော်လင့်ထားတဲ့အဖြေပဲရလာခဲ့ပါတယ်။