## Arrow Function

Javascript မှာ function ရေးထုံးအနေနဲ့ နှစ်မျိုးရေးလို့ရတယ်လို့ပြောလို့ရတယ် ။ ပထမ တစ်နည်းက function name  ပါတာ  နဲ့  function name မပါတဲ့ Anonymous or Nameless function  လို့ခေါ်ကြတယ်။ 

**Example - 1**

```javascript
function getName(*name*) {

​	console.log(*name*);

}

getName("Batman");	 **Answer => Batman**
```

**Example - 2**

```
let getName = function (*name*) {

  console.log(*name*)

}

getName("Batman");	**Answer => Batman**
```

အပေါ်က example ၂ ခုမှာ ပထမတစ်ခုက Function name ပါတာ နဲ့ ဖစ်ပီး  နောက်တစ်ခုက Nameless or Anonymous Function ဖစ်တယ်။  Javascript မှာ  Anonymous Function  ရေးနည်းကိုသာတော်တော်များများသုံးကြပါတယ်။ React ရောက်ရင်လဲ နေရာနီးပါးတိုင်းမှာ Anonymous Function ကိုသာမြင်ရမှာမို့အခုကတဲသေချာကြည့်ထားစေချင်ပါတယ်။ 

**Example - 3**

```
let superHero = {

  name: "Batman",

  city: "Gotham",

  getName: function () {

​    console.log("Super hero name is " + this.name);

   }

}

superHero.getName();	**Answer => Super hero name is Batman**
```



example 3 မှာဆိုပုံမှန် Javascript object တစ်ခုမှာ name, city ဆိုတဲ့ variables 2 ခုရယ် getName ဆိုတဲ့ function တစ်ခုရယ်ပါတယ်။ သာမာန်  javascript object လေးတစ်ခုပဲ။ အာ့ဆို အဲ့ object လေးထဲက getName ဆိုတဲ့ function ထဲမှာ နောက်ထပ် function တစ်ခုထပ်ထည့်ကြည့်လိုက်ရအောင်...

**Example - 4**

```
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

**Answer 1 => Super hero name is Batman**

**Error => Super hero name is undefined City is undefined**
```



