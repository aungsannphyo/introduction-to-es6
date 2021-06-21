## Default Parameter and Rest Parameter

#### 1 - Default Parameter

default parameter ဆိုတာ es6 မှာမှစပါလာတဲ့ လုပ်ဆောင်ချက်တစ်ခုဖစ်ပါတယ်။ 

`Example - 1`

```javascript
const getName = (name) => {
    console.log(name)
}

getName(); // => undefinded
```

example 1 မှာဆိုရင် getName() func ကိုခေါ်တဲ့အခါမှာ arugment တစ်ခုကိုထည့်ပေးရမဲ့အစားထည့်မပေးပဲခေါ်လိုက်တော့ undefined ဆိုပီး error တက်သွားတာမြင်ရလိမ့်မယ်။ getName() ကိုခေါ်တဲ့အချိန် String name တစ်ခုခုသာထည့်ပေးခဲ့ရင် error တက်စရာမလိုပဲ အဖြေရပါလိမ့်မယ်။ ဒါပေမဲ့ ကျွန်တော်တို့က argument ထည့်မပေးပဲလဲရေးလို့ရပါသေးတယ်။

`Example - 2`

```javascript
const getName = (name = "Batman") => {
    console.log(name)
}

getName(); // => Batman
getName("Super Man"); // => Superman
```

example 2  မှာဆိုရင် parameter မထည့်ပဲခေါ်လိုက်တဲ့အချိန်မှာ error မတက်ပဲ အလုပ်လုပ်သွားတာမြင်ရလိမ့်မယ် ဘာလို့လဲဆိုတော့ Function မှာ default အနေနဲ့ Batman ဆိုပီးပေးထားလိုက်တဲ့အတွက်ဖစ်ပါတယ်။ အောက်က getName မှာ Superman ဆိုပီးပေးပီးသုံးလိုက်ရင်တော့ကျွန်တော်တို့မျှော်လင့်ထားသလို အလုပ်လုပ်သွားတာဖစ်ပါတယ်။ 

#### 2 - Rest Parameter

Rest Parameter ဆိုတာကတော့ Function တစ်ခုမှာ parameter အရေအတွက်ကိုအတိအကျမသိဘူး အသေလဲမသတ်မှတ်ချင်တော့ဘူး ဆိုရင် ကိုယ်ပေးချင်သလောက်ပေး အကုန်လက်ခံပီးသုံးမယ်ဆိုတဲ့အခါမှာ rest parameter ကအရမ်းအသုံး၀င်ပါတယ်။

`Example - 3`

```javascript
const getSuperHeroDetails = (company, ...name) => {
    console.log(name)
}

getSuperHeroDetails("Marvel", "Ironman", "Spiderman", "Hulk", "Loki"); 
Answer => [ 'Ironman', 'Spiderman', 'Hulk', 'Loki' ]
```

အပေါ်က example 3 မှာဆိုရင် အရှေ့ဆုံးကပေးထားတဲ့ Marvel က company ဆိုတဲ့ parameter အတွက်ဖစ်သွားပီး အနောက်ကျန်တဲ့အရာတွေအားလုံးကတော့ Array အနေနဲ့ name အတွက်ဖစ်သွားတာကိုမြင်ရမှာဖစ်ပါတယ်။ များများချရေး လက်တွေ့လုပ်ဖို့လဲဒီကနေအကြံပေးပါတယ်။ 
