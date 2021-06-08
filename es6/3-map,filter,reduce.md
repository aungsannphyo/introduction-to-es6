## Map, Filter, Reduce

#### 1.Map

`Example - 1`

```javascript
let superHero = ["batman", "superman", "flash", "wonder woman"];

superHero.forEach((hero) => {
    console.log(hero)
})

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
const numArray = [1, 2, 3, 4];

let result = numArray.reduce((prev, current) => prev + current)

console.log(result)

Answer => 10
```

 Example 5 မှာဆိုရင်  reduce() ရဲ့  callback Function မှာသူကကျ Argument မှာ ပထမတစ်ခုက previousValue အရင်တန်ဖိုးနဲ့ currentValue လက်ရှိတန်ဖိုးဆိုပီး တန်ဖိုး၂ ခုလက်ခံတယ်။ အပေါ်က example မှာဆိုရင် အရင်တန်ဖိုးကို လက်ရှိတန်ဖိုးနဲ့ ပေါင်းပေါင်းသွားတဲ့အတွက် နောက်ဆုံးမှာ အားလုံးပေါင်းတန်ဖိုးရတာဖစ်တယ်။ဘယ်လိုရလဲဆိုတာရှင်းပြပေးပါမယ်။ ပထမဆုံး စစအလုပ်လုပ်ချင်းမှာ prev တန်ဖိုးက 1 current  တန်ဖိုးက  2 ဖစ်နေတယ် သူတို့ပေါင်းခြင်းက  3။ ဒုတိယတစ်ခေါက်အလုပ်လုပ်တဲ့ချိန်ကျ prev တန်ဖိုးက  3  current က 3 ပေါင်းခြင်းက 6 ။ အဲ့လိုနဲ့နောက်ဆုံးမှာပေါင်းခြင်း 10 ရသွားတယ် အမလေး trace လိုက်ပေးရတာမောတာ .... ဒီ reduce() function ကိုသေချာနားလည်အောင်ကြည့်ထားစေချင်ပါတယ် အရမ်းအသုံး၀င်ပီး Redux , Context Provider ( State Management ) တွေကျရင်သူကိုပဲအဓိကထားသုံးတာမြင်ရမှာမို့လို့ပါ.... 