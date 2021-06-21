## Destructuring , Spread Operator && Optional Chaining

#### 1 - Destructuring

အလွယ်ပြောရရင် destructuring  ဆိုတာ array တွေ object တွေကို ဖြည်ချတဲ့သဘောပဲပါပဲ

`Example - 1`

```javascript
let name = ["batman", "superman"]

console.log(name[0]); // => batman
console.log(name[1]); // => superman
```

`Example - 2`

```javascript
let name = ["batman", "superman"]

let [batman, superman] = name;

console.log(batman); // => batman
console.log(superman); // => superman
```

example 1 မှာဆိုရင် array ထဲက value တွေကိုလိုချင်တဲ့အခါကျွန်တော်တို့က loop ပတ်ပီးယူခဲ့ကြသလို အခုလို index ထောက်ပီးလဲယူခဲ့ကြတယ် ပုံမှန်ရေးနည်းပါပဲ။  example 2 မှာကျ တော့ name ဆိုတဲ့ array ကို destructure လုပ်ပီးရေးလိုက်တဲ့ပုံကိုရေးပြထားတာဖစ်ပါတယ်။ အာ့ဆို object ဆိုရင်ရောဘယ်လိုရေးလဲကြည့်လိုက်ရအောင်

`Example - 3`

```javascript
let superHero = { name: "batman", company: "DC" }

console.log(superHero.name) // => batman
console.log(superHero.company) // => DC

//destructure
let { name, company } = superHero
console.log(name) // => batman
console.log(company) // => DC
```

Array and Object အပြင် Function နဲ့ဘယ်လိုတွဲသုံးလဲဆိုတာကြည့်လိုက်ရအောင်

`Example - 4`

```javascript
function getSuperHero(superHero) {
    console.log(`My name is ${superHero.name} and my original name is ${superHero.originalName}`)
}

getSuperHero({ name: "Batman", originalName: "Bruce Wayne" })
Answer => My name is Batman and my original name is Bruce Wayne

//destructure
function getSuperHero({ name, originalName }) {
    console.log(`My name is ${name} and my original name is ${originalName}`)
}

getSuperHero({ name: "Batman", originalName: "Bruce Wayne" })
Answer => My name is Batman and my original name is Bruce Wayne
```

#### 2 - Spread Operator

spread လုပ်တယ်ဆိုတာက array , string စတဲ့ iterable  ဖစ်နေတဲ့ value တွေကို ခွဲ့ဖြန့်ပေးနိုင်တာကိုခေါ်ပါတယ်။ ကဲ example နဲ့ကြည့်လိုက်ရအောင်

`Example - 5`

```javascript
let name = ["aung aung", 'mg mg']
let age = [21, 20]

let combineOne = name.concat(age)
let combineTwo = [name, age]
let combineThree = [...name, ...age]

console.log(combineOne) // => [ 'aung aung', 'mg mg', 21, 20 ]
console.log(combineTwo) // => [ [ 'aung aung', 'mg mg' ], [ 21, 20 ] ]
console.log(combineThree) // => [ 'aung aung', 'mg mg', 21, 20 ]
```

example 5 မှာဆိုရင် combineOne က ကျွန်တော်တို့ပုံမှန်သိထားတဲ့ js ရဲ့ concat method ကိုခေါ်သုံးပီးရေးထားတဲ့နာမူနာဖစ်ပါတယ်။ combineTwo မှာဆိုရင်တော့ ကျွန်တော်တို့က  array ထဲမှာ name and age arrays တွေကိုထည့်လိုက်တဲ့အတွက် array နှစ်ထပ်ဖစ်သွားတာကိုမြင်ရပါလိမ့်မယ်။  combineThree မှာဆိုရင် array ထဲမှာ name and age arrays ထည့်တာချင်းတူတူကို အရှေ့မှာ (...) ဆိုတဲ့ spread operator ပါလာတဲ့အတွက် name and age ဆိုတဲ့ array ကိုဖြန့်ချလိုက်တာကြောင့်ကျွန်တော်တို့လိုချင်သလို array နှစ်ခုတစ်ဆက်ထဲဖစ်သွားတာကိုမြင်ရမှာပါ။ အရမ်းကိုအသုံး၀င်တဲ့အရာဖစ်လို့သေချာကြည့်ထားစေချင်ပါတယ်။ 



