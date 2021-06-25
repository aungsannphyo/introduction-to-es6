## Classes and Constructor

Javascript ဟာပြောရရင် Prototype OOP လိုခေါ်လို့ရတယ်ဗျဘာလို့လဲဆိုသူမှာ Class base OOP မဟုတ်တဲ့အတွက် Object တွေကိုတည်ဆောက်မယ်ဆိုရင် Class ကိုသုံးလိုမရပဲ Object constructor and JSON တို့ကိုသာအသုံးပြုပီးတည်ဆောက်လို့ရတယ်။ကဲအဲ့တာက ဘယ်လိုလဲဆိုတာ နမူနာကြည့်ရအောင်

`Example - 1 `

```javascript
function Superhero(name, age){
	this.name = name;
    this.age = age;
}

Superhero.prototype.sayName = function(){
    console.log("My name is " + this.name);
}

var batman = new Superhero("Batman", "30");

console.log(batman); // => Superhero { name: 'Batman', age: '30' }
batman.sayName(); // => My name is Batman
```

Example 1 ကိုကြည့်ရရင်အရင် အရင်ကဘယ်လိုတည်ဆောက်ရသလဲဆိုတာ example အနေနဲ့ရေးပြထားတာဖစ်ပါတယ်။ ES6 ရောက်လာတဲ့ချိန်မှာတော့အဲ့လိုရေးစရာမလိုပဲ Class ကိုစတင်အသုံးပြုလို့ရလာပါပီ။ 

 `Example - 2`

```javascript
class Superhero {
	constructor (name,age){
        this.name = name;
        this.age = age;
    }
    sayName(){
        return `My name is ${this.name}`
    }
}
```

ကျွန်တော်တိုသိနေတဲ့တခြား OOP ရေးထုံးတွေနဲ့သိပ်မကွာပါဘူး သူမှာတစ်ခုရှိတာက ES6 အနေနဲ့စစထွက်ပေါ်ကစမှာ property တွေကိုတိုက်ရိုက် declare  လို့မရပဲ constructor အတွင်းကနေပဲ this keyword ကတဆင့်ခံကြေညာပေးလို့ရတယ်။ နောက်တစ်ခုက သူတို့မှာ private, public စတဲ့ Access Modifier တွေမရှိပါဘူး Function တွေကြေညာတဲ့အချိန်မှာလဲ function keyword ကိုထည့်ပေးစရာမလိုတော့ကိုသိထားစေချင်ပါတယ်။ နောက်ပိုင်းမှတော့တိုက်ရိုက်ရေးလို့ရအောင်လုပ်ပေးတဲ့ လုပ်ဆောင်ချက်ပါ၀င်လာတဲ့အတွက် Property တွေကိုတိုက်ရိုက်ရေးသားလို့ရသလို Function တွေပါ class field အနေနဲ့ရေးသားလို့ရလာပါတယ်။ 

`Example - 3`

```javascript
class Superhero {
    name = "Batman";

    sayName = () => `My name is ${this.name}`
}

let batman = new Superhero();
batman.name; // => Batman
batman.sayName(); // => My name is Batman
```

Example 3 မှာဆိုရင် name ကို တိုက်ရိုက်ကြေညာထားတာဖစ်ပါတယ်။ နောက်တစ်ခုအနေနဲ့  sayName ဆိုတဲ့အရာကတန်ဖိုးတစ်ခုမဟုတ်ပဲ Array Function  ဖစ်နေလို့ function အနေနဲ့အသုံးပြုရတာဖစ်တယ်ဗျ။ 