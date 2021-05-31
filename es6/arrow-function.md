## Arrow Function

Javascript မှာ function ရေးထုံးအနေနဲ့ နှစ်မျိုးရေးလို့ရတယ်လို့ပြောလို့ရတယ် ။ ပထမ တစ်နည်းက function name  ပါတာ  နဲ့  function name မပါတဲ့ Anonymous or Nameless function  လို့ခေါ်ကြတယ်။ 

**Example - 1**

```javascript
function getName(*name*) {

​	console.log(*name*);

}

getName("Batman");	 Answer => Batman
```

**Example - 2**

```javascript
let getName = function (*name*) {

  console.log(*name*)

}

getName("Batman");	 Answer => Batman
```

အပေါ်က example ၂ ခုမှာ ပထမတစ်ခုက Function name ပါတာ နဲ့ ဖစ်ပီး  နောက်တစ်ခုက Nameless or Anonymous Function ဖစ်တယ်။  Javascript မှာ  Anonymous Function  ရေးနည်းကိုသာတော်တော်များများသုံးကြပါတယ်။ React ရောက်ရင်လဲ နေရာနီးပါးတိုင်းမှာ Anonymous Function ကိုသာမြင်ရမှာမို့အခုကတဲသေချာကြည့်ထားစေချင်ပါတယ်။ 

**Example - 3**

```javascript
let superHero = {

  name: "Batman",

  city: "Gotham",

  getName: function () {

​    console.log("Super hero name is " + this.name);

   }

}

superHero.getName();	Answer => Super hero name is Batman
```



example 3 မှာဆိုပုံမှန် Javascript object တစ်ခုမှာ name, city ဆိုတဲ့ variables 2 ခုရယ် getName ဆိုတဲ့ function တစ်ခုရယ်ပါတယ်။ သာမာန်  javascript object လေးတစ်ခုပဲ။ အာ့ဆို အဲ့ object လေးထဲက getName ဆိုတဲ့ function ထဲမှာ နောက်ထပ် function တစ်ခုထပ်ထည့်ကြည့်လိုက်ရအောင်...

**Example - 4**

```javascript
let superHero = {

  name: "Batman",

  city: "Gotham",

  getName: function () {

​    console.log("Super hero name is " + this.name);

​    function getDetails() {

​      console.log("Super hero name is " + this.name + " City is " + this.city);

​    }

 getDetails();

  }

}

superHero.getName()	

Answer => Super hero name is Batman

Error => Super hero name is undefined City is undefined
```

Example 4 မှာဆို superHero.getName() ဆိုပီး function ကိုခေါ်လိုက်တဲ့အချိန်မှာ ပထမက Name ရတယ် ဒုတိယ getDetails() function ထဲက name and city ကိုမသိတော့ပဲ undefined တွေဖစ်ကုန်တယ်။ အဲ့တာဘာလို့ဖစ်လဲဆိုတော့ javascript မှာ this ပြဿနာကအဲ့လိုပဲ ကြုံရတက်တယ်။ ဘာလို့ဖစ်လဲဆိုတော့က  တခြား programming language တွေလေ့လာဖူးရင်သိလိမ့်ကြမယ်။ အပေါ်က Example 4 မှာ this ကိုနှစ်နေရာတွေ့ရတယ် ပထမ this.name က သူ့ parent superHero ဆိုတဲ့ variable ကိုညွှန်းတဲ့အတွက်အဖြေရတယ်။ ဒုတိယ this က အမှန်ဆို parent superHero ကိုပဲညွှန်းရမှာ ဒါပေမဲ့ သူရောက်နေတာက getName() ဆိုတဲ့ function ထဲရောက်နေတော့ သူ့ parent က getName() ဆိုတဲ့ function ဖစ်သွားပီး name and city ကိုသူကမတွေ့တော့ပဲ undefined ဆိုပီး error တက်သွားတာ။ အဲ့ error ကိုဘယ်လိုရှင်းလဲဆိုရင်....

**Example - 5**

```javascript
let superHero = {

  name: "Batman",

  city: "Gotham",

  getName: function () {

​    console.log("Super hero name is " + this.name);
	
      let hero = this;
      
​    function getDetails() {

​      console.log("Super hero name is " + hero.name + " City is " + hero.city);

​    }

 getDetails();

  }

}

superHero.getName()	

Answer => Super hero name is Batman

Answer => Super hero name is Batman City is Gotham
```

Example 5 မှာဆိုရင် အပေါ်ကပြောခဲ့သလို this ကို ခေါ်သုံးလို့ရတာ getName() ဆိုတဲ့ function ထဲကနေသုံးလို့ရတယ် အဲ့တော့ကျွန်တော်က hero ဆိုတဲ့ variable declare လုပ်ပီး အဲ့ hero ထဲ this ကိုထည့်လိုက်တယ်။ အဲ့ကျ hero.name and hero.city  ဆိုပီးခေါ်သုံးလိုက်တော့ error မတက်တော့ပဲ အဖြေထွက်လာတယ်။ နည်းနည်းရူးကြောင်ကြောင်နိုင်တယ် ဟုတ်တယ်မလား  ::stuck_out_tongue_winking_eye: . အခုလိုတွေ this ပြဿနာမကြုံရအောင် ES6 မှာပါလာတဲ့ Arrow Function ကိုသုံးပီးရေးကြည့်ရအောင်။ 

**Example - 6**

```javascript
let superHero = {
    name: "Batman",
    city: "Gotham",
    getName: function () {
        console.log(`Super hero name is ${this.name}`);
        getDetails = () => {
            console.log(`Super hero name is ${this.name} City is ${this.city}`)
        }
        getDetails()
    }
}

superHero.getName()

Answer => Super hero name is Batman

Answer => Super hero name is Batman City is Gotham
```

Example 6 မှာ ပထမ console.log မှာအဖြေထုတ်တဲ့ပုံစံပြောင်းလဲသွားတယ် အပေါ်မှာရေးခဲ့သလို + နဲ့ရေးရတာကြည့်ရရှုပ်သလိုအဆင်မပြေလှဘူး အခုလို `` သုံး ${this.name} ဆိုပီးပြောင်းလဲရေးလိုရလာတဲ့ အဲ့လိုရေးနည်းကိုဘယ်လိုခေါ်လဲဆိုတော့ **String Interpolation** လိုခေါ်ပီး ES6 ရဲ့ feature တစ်မျိုးဖစ်တယ်။ ဟုတ်ပီ အာ့ဆိုရင် getDetails() မှာလဲ အပေါ်ကလိုမဟုတ်တော့ပဲ Arrow Function ကိုသုံးလိုက်တော့ ကျွန်တော်တို့ကြုံရတဲ့ this ပြဿနာမကြုံရတော့ပဲ အဖြေတန်းရသွားတယ်။

**Example - 7**

```
getName = () => console.log("I am Batman")

getName();	 Answer => I am Batman
```

Example 7 မှာလို တကယ်လိုသူ့မှာတစ်ကြောင်းထဲပါတယ်ဆိုရင် အခုလိုတိုက်ရိုက် { } မပါဘဲလဲတန်းရေးလိုလဲရတယ်။